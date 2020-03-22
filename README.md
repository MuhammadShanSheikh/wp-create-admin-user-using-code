# wp-create-admin-user-using-code

// Create admin user using code
add_action( 'init', function () {
	$username = 'admin2';
	$password = 'admin';
	$email_address = '';
	if ( ! username_exists( $username ) ) {
		$user_id = wp_create_user( $username, $password, $email_address );
		$user = new WP_User( $user_id );
		$user->set_role( 'administrator' );
	}
} );
