# Remember to change mydomain.com with your correct domain and /contact/ with your Contact Form URLS

## Rule to block SPAM in contact forms
``
(http.request.version in {"HTTP/1.0" "HTTP/1.1" "HTTP/1.2"} 
and http.request.uri eq "/contact/" 
and not http.user_agent contains "Googlebot" 
and not http.user_agent contains "Bingbot" 
and not http.user_agent contains "DuckDuckBot" 
and not http.user_agent contains "facebot" 
and not http.user_agent contains "Slurp" 
and not http.user_agent contains "Alexa")
``

## Another rule to block SPAM in contact forms and comments, you can combine with previous rules
`(http.request.uri contains "/wp-admin/admin-ajax.php" and http.request.method eq "POST" and not http.referer contains "mydomain.com") or (http.request.uri contains "/wp-comments-post.php" and http.request.method eq "POST" and not http.referer contains "mydomain.com")`

## Two previous rules combined
``
(http.request.version in {"HTTP/1.0" "HTTP/1.1" "HTTP/1.2"} 
and http.request.uri eq "/contact/" 
and not http.user_agent contains "Googlebot" 
and not http.user_agent contains "Bingbot" 
and not http.user_agent contains "DuckDuckBot" 
and not http.user_agent contains "facebot" 
and not http.user_agent contains "Slurp" 
and not http.user_agent contains "Alexa") or
(http.request.uri contains "/wp-admin/admin-ajax.php" and http.request.method eq "POST" and not http.referer contains "mydomain.com") or
(http.request.uri contains "/wp-comments-post.php" and http.request.method eq "POST" and not http.referer contains "mydomain.com")
``