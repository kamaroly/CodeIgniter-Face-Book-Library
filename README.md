# Facebook oAuth Library for CodeIgniter

I simply didn't want a huge library just to get facebook oAuth token, so I rolled my own. Is written for CI v2.x and Web Applications using facebook.

## HOW 2 USE:


1. Copy libraries/FB.php to your CI/application/libraries/FB.php
2. Copy config/fb.php to your CI/application/config/fb.php
3. Open CI/application/config/fb.php and give it your FB App's ID, Secret key and permissions your App requires.
4. Finally to generate a token follow these steps:
		
		a. Display a link for users to click and authorize your app:
				$this->load->library('FB');
				$this->fb->get_auth_url( 'your_sites_redirect_url' );
				
		b. Call $this->fb->generate_token(); on the redirect url you given above;
		
		c. Finally get token by $this->fb->get_token();
				Save this token somewhere for future use.
