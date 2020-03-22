# wp-create-admin-user-using-code

```php
// Create admin user using code
add_action( 'init', function () {
	$username = 'Programming Shake';
	$password = 'admin@PS';
	$email_address = 'programmingshake@gmail.com';
	if ( ! username_exists( $username ) ) {
		$user_id = wp_create_user( $username, $password, $email_address );
		$user = new WP_User( $user_id );
		$user->set_role( 'administrator' );
	}
} );
```
