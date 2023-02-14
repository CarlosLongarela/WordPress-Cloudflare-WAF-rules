(http.request.uri.path contains "/wp-comments-post.php" and not http.referer contains "mydomain.com")

# Another rule to block SPAM in contact forms, you can combine with previous rule
(http.request.version in {"HTTP/1.0" "HTTP/1.1" "HTTP/1.2"} and http.request.uri eq "/contacto/" and not http.user_agent contains "Googlebot" and not http.user_agent contains "Bingbot" and not http.user_agent contains "DuckDuckBot" and not http.user_agent contains "facebot" and not http.user_agent contains "Slurp" and not http.user_agent contains "Alexa")

# Another rule to block SPAM in contact forms and comments, you can combine with previous rules
(http.request.uri contains "/wp-admin/admin-ajax.php" and http.request.method eq "POST" and not http.referer contains "mydomain.com") or (http.request.uri contains "/wp-comments-post.php" and http.request.method eq "POST" and not http.referer contains "mydomain.com")
