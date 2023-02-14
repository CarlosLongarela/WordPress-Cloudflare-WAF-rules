<code>
(cf.threat_score gt 14) or 
(cf.threat_score gt 10 and cf.client.bot) or
(http.request.uri.query contains "author_name=" and not http.request.uri.path contains "/wp-admin/") or 
(http.request.uri.query contains "author=" and not http.request.uri.path contains "/wp-admin/") or 
(http.request.uri contains "/wp-json/wp/v2/users/" and not http.referer contains "/wp-admin/") or 
(http.request.uri contains "wp-config.") or (http.request.uri contains "setup-config.") or 
(http.request.uri.path contains ".js.map") or  
(lower(http.request.uri.path) contains "phpmyadmin") or 
(lower(http.request.uri.path) contains "thinkphp") or 
(http.request.uri.path contains "/phpunit") or 
(raw.http.request.uri contains "../") or (raw.http.request.uri contains "..%2F") or 
(http.request.uri contains "passwd") or 
(http.request.uri contains "/dfs/") or 
(http.request.uri contains "/autodiscover/") or 
(http.request.uri contains "/wpad.") or 
(http.request.uri contains "/wallet.dat") or 
(http.request.uri contains "webconfig.txt") or 
(http.request.uri contains "vuln.") or 
(http.request.uri contains ".env") or (http.request.uri contains ".ini") or (http.request.uri contains ".log") or (http.request.uri contains ".sql") or
(http.request.uri.query contains "bin.com/") or (http.request.uri.query contains "bin.net/") or (raw.http.request.uri.query contains "?%00") or 
(http.request.uri.query contains "eval(") or (http.request.uri.query contains "base64") or (http.request.uri.query contains "var_dump") or 
(http.request.uri.query contains "<script") or (raw.http.request.uri.query contains "%3Cscript") or 
(http.request.full_uri contains "<?php") or 
(http.cookie contains "<?php") or 
(http.cookie contains "<script") or (http.referer contains "%3Cscript") or 
(http.cookie contains "base64") or (http.cookie contains "var_dump") or 
(upper(http.request.uri.query) contains "$_GLOBALS[") or 
(upper(http.request.uri.query) contains "$_REQUEST[") or 
(upper(http.request.uri.query) contains "$_POST[")
</code>
