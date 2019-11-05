## Remove Google reCAPTCHA v3 badge
You can found a full article on this argument here [EE here](https://www.experts-exchange.com/articles/33413/How-to-remove-the-annoying-Google-reCAPTCHA-v3-badge-from-your-website-without-breaking-the-rules.html) 
You are allowed to hide the badge as long as you include the reCAPTCHA branding visibly in the user flow : 
```html
<p>This site is protected by reCAPTCHA and the Google
    <a href="https://policies.google.com/privacy">Privacy Policy</a> and
	<a href="https://policies.google.com/terms">Terms of Service</a> apply.</p>
```
So once we have notified user about Google reCAPTCHA privacy and T&C we can remove the captcha by adding the follow CSS code :
```css
/* Hide the Google reCAPTCHA badge, but note this requires a link to the Google T&C's to be added
  to contact forms. See https://developers.google.com/recaptcha/docs/faq for details. */
  .grecaptcha-badge { display: none; }
  .custom-recaptcha3-terms { font-size:12px; }
```



AJAX call WordPress
All the ajax call in wordpress will be directed to the admin.php file.
// ajax
wp_localize_script( 'name of the JS file', 'ajax_object',    array( 'ajax_url' => admin_url( 'admin-ajax.php' ) , 'nonce' => wp_create_nonce( 'nonce_name' ) ) );
