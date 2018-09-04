<?php

/*
Plugin Name: WP-PHPMailer Peer Verification Disabler
Plugin URI: http://www.joaoneto.blog.br
Description: Peer Verification Disabler for error websites
Version: 1.0
Author: Joao Neto
Author URI: http://www.joaoneto.blog.br
*/


function phpmailer_wp_smtp_disable_peer_verification( $phpmailer ) {

  $phpmailer->SMTPOptions = array(
    'ssl' => [
        'verify_peer' => false,
        'verify_depth' => 3,
        'allow_self_signed' => true
	]
   );

  return $phpmailer;
}

add_filter( 'wp_mail_smtp_custom_options', 'phpmailer_wp_smtp_disable_peer_verification', 2 );
