<h1>How to create custom post type</h1>
<pre>
function my_custom_event() {
  $labels = array(
    'name'               => _x( 'Events', 'post type general name' ),
    'singular_name'      => _x( 'Events', 'post type singular name' ),
    'add_new'            => _x( 'Add New', 'Events' ),
    'add_new_item'       => __( 'Add New Events' ),
    'edit_item'          => __( 'Edit Events' ),
    'new_item'           => __( 'New Events' ),
    'all_items'          => __( 'All Events' ),
    'view_item'          => __( 'View Events' ),
    'search_items'       => __( 'Search Events' ),
    'not_found'          => __( 'No Events found' ),
    'not_found_in_trash' => __( 'No Events found in the Trash' ), 
    'parent_item_colon'  => '',
    'menu_name'          => 'Events'
);

$args = array(
    'labels'        => $labels,
    'description'   => 'Events',
    'public'        => true,
    'show_ui'        => true,
    'capability_type'  => 'post',
    'menu_position' => 5,
    'supports'      => array( 'title' , 'thumbnail', 'editor', 'page-attributes'),
    'has_archive'   => true,
);   

register_post_type( 'event', $args );   
}
add_action( 'init', 'my_custom_event' );
</pre>
