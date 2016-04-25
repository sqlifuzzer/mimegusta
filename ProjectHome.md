![http://securitytheatre.files.wordpress.com/2012/12/mimegusta.jpg](http://securitytheatre.files.wordpress.com/2012/12/mimegusta.jpg)

## WTF? ##

MIMeGusta is a configurable content-sniffing XSS testbed. Content-sniffing XSS mainly applies to vulnerable file upload implementations, where an attacker is able to upload files with embedded client-side code such as JavaScript with the objective of XSS-ing users of the hosting domain.

MITRE define this form of XSS as [CAPEC-209: Cross-Site Scripting Using MIME Type Mismatch](http://capec.mitre.org/data/definitions/209.html), OWASP describe it [here](https://www.owasp.org/index.php/Testing_for_Stored_Cross_site_scripting_(OWASP-DV-002)) (scroll down to the File Upload part).

MIMeGusta is intended to allow security testers to explore the behaviour of browsers with particular focus upon the role of content-sniffing 'cues' in determining whether JavaScript will be executed.

Rather than upload/download countless variations of files, MIMeGusta allows you to configure a range of headers which are included with a JavaScript alert box payload response. It can also include a range of file signatures, defensive headers, as well as inserting file type path info into the URL. It also includes two filters: one
examines content-type headers, while the other analyses content-type headers AND file
signatures. Both filters have a 'weak' (i.e circumventable) and 'strong' mode.

MIMeGusta also includes a small number of challenges intended to demonstrate some basic content-sniffing XSS techniques.

MIMeGusta challenges currently focus entirely upon Internet Explorer 9 with the XSS filter enabled. Other browsers and earlier versions of IE are also subject to content sniffing based XSS attacks, but you've gotta start somewhere :-)

## Requirements ##
PHP 5.x

Web server. Apache works fine.

Challenges are written to work for Internet Explorer 9 and likely cannot be completed in other browsers, though earlier versions of IE are likley to work.

## Usage ##

Place the MIMeGusta source files on your Web server and
open in Internet Explorer.

## Thanks ##

Thanks to those who have released vulnerable test-beds such as XMLmao,
SQLol, CryptOMG, XSSmh, ShelLOL, etc, etc.

## Also ##

If you like MIMeGusta, check out:

[sqlifuzzer](http://code.google.com/p/sqlifuzzer/)

[The Manipulator](http://code.google.com/p/the-manipulator/)