--- 
layout: post 
title: "Error 1044 in MySQL: Access denied when using LOCK TABLES"
description: ""
category: "Archive"
tags: []
---
{% include JB/setup %}  
Had some issues during a standard mysqldump. I've never encountered it before, and I've made similar dumps on identical mysql servers all day. Basically, it auto sets to lock tables somehow. It is a reported <a href="http://bugs.mysql.com/bug.php?id=21527" rel="nofollow">bug at MySQL</a>, and the page states that the bug is closed. According to the <a href="http://forums.mysql.com/read.php?10,108835,108835#msg-108835" rel="nofollow">forums at MySQL</a> it seemed to be an easy fix; 

<pre class="brush: sql">
GRANT SELECT,LOCK TABLES ON database.* TO 'username'@'localhost'; 
</pre>

But I double checked, the user had ALL priviliges (yeah, not that safe). The same post mentioned above had a simpler solution that worked brilliantly:

<pre class="brush: sql">
mysqldump -u username -p database --single-transaction >dump.sql
</pre>
