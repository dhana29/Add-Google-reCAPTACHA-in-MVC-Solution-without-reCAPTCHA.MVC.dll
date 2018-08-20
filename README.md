# Add-Google-reCAPTACHA-in-MVC-Solution-without-reCAPTCHA.MVC.dll
Add Google reCAPTACHA in MVC Solution without reCAPTCHA.MVC.dll

**Steps:**

1) Generate key from the below path 
https://www.google.com/recaptcha/admin


2) Create ASP .Net MVC Template solution
3) Add View, Controller and Model code from the attachment
4) Important to add below lines in the web.config file
   ```   
     <appSettings>
        <add key="UnobtrusiveJavaScriptEnabled" value="true" />
        <add key="reCaptchaPublicKey" value="CopyPublicKeyFromGoogleCAPTACHA" />
        <add key="reCaptchaPrivateKey" value="CopyPrivateKeyFromGoogleCAPTACHA" />
    </appSettings>
    
    <handlers>
      <add name="MSCaptcha" verb="GET" path="CaptchaImage.axd" type="MSCaptcha.CaptchaImageHandler, MSCaptcha"/>
    </handlers>
    
HAPPY CODING!
