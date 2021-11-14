# Kirki Simple Gradient

**Author      :** Ravi Shakya  
**Author URI  :** https://bizbergthemes.com  
**License     :** GNU General Public License v2 or later  
**License URI :** http://www.gnu.org/licenses/gpl-2.0.html  
**Version     :** 0.2

## Description ##

Use this control to add gradient colors

![image](https://user-images.githubusercontent.com/11089018/139005468-22be15be-4213-49ef-b287-e08486e2d7af.png)

## Example Code ##

````php
add_action( 'init' , function(){

	Kirki::add_field( 'bizberg', array(
		'type'        => 'simple-gradient',
		'label'       => 'Body Background',
		'section'     => 'detail_page',
		'settings'    => 'body_background_gradient',
		'description' => 'Simple Gradient Selector',
		'default'     => 'linear-gradient(291deg, #dd9933, #b24e23)', // Use only hex colors
		'transport'   => 'auto',
		'output' => array(
			array(
				'element'  => 'body',
				'property' => 'background',
			)
		),
	) );
});
````

## How to get color in frontend ? ##
````php
$body_background = get_theme_mod( 'body_background_gradient' );
echo esc_attr( $body_background );
````

**Parameters**  

**default** - (string) (optional) Eg: `linear-gradient( 291deg, #dd9933, #b24e23 )` , `radial-gradient( circle, #dd9933, #b24e23 )`

## Note ##
You will need to install the kirki plugin first https://wordpress.org/plugins/kirki/

## Changelog ##

= 0.2 =
- Fixed prefix

= 0.1 =
- Initial Release
