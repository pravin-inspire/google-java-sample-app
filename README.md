SendGrid on Google App Engine
======================

This git repository helps you to send emails quickly and easily through SendGrid on Google App Engine using Java.


Running on Google App Engine
----------------------------

Create an SendGrid account at http://sendgrid.com/pricing.html

Create an account at https://appengine.google.com/ and set up your local machine with the client tools https://developers.google.com/appengine/docs/java/gettingstarted/installing

Create an application at https://appengine.google.com/start/createapp

Clone SendGrid application on your local machine
<pre>
    git clone https://github.com/sendgrid/google-java-sample-app
</pre>

###Configuration###

Configure `GoogleSendgridJava/src/googleSendgridJava/GoogleSendgridJavaServlet.java` file with your information:

Update the *&lt;sendgrid_username&gt;* and *&lt;sendgrid_password&gt;* with your SendGrid credentials.
```Java
    Sendgrid mail = new Sendgrid("<sendgrid_username>","<sendgrid_password>");
```
Update the *&lt;from_address&gt;* with your email address
```Java
    .setFrom("<from_address>")
```
Update application identifier in `GoogleSendgridJava/war/WEB-INF/appengine-web.xml` file
```XML
    <application>application_identifier</application>
```

Upload your application to Google App Engine: https://developers.google.com/appengine/docs/java/gettingstarted/uploading

That's it, you can now checkout your application at:
<pre>
    http://application_identifier.appspot.com/
</pre>




