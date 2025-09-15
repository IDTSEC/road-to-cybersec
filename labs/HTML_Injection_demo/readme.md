# HTML Injection Demo

## what i did
- built a simple page (vuln.html) that reflects input from '?q='
- injected a link: '?q=<a href="http://example.com">wow, you won!</a> -> html injection done

## why related to SOC?
- attackers use it for phishing (injecting links)/XSS
- SOC analysts look for encoded '<a href'/'<script>' in logs
- demonstrates why **input sanitization** is crucial

## solution?
- escape '<' and '>' before printing input ('safe.html')
- from now, the browser will stop interpreting user input as HTML

## files used
- [initial vulnerability file](vu;m
