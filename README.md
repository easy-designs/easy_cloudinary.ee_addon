Easy Cloudinary for ExpressionEngine
====================================

ExpressionEngine Plugin to automate use of the Cloudinary.

Setting it up
-------------

All configuration of this plugin happens in your ExpressionEngine Configuration file:

```php
$config['easy_cloudinary'] = array(
  'cloud_name' => 'YOUR_CLOUDINARY_CLOUD_NAME',
  'template'   => '<img src="https://res.cloudinary.com/{cloud_name}/image/fetch/f_auto,q_auto/{image_url}" {attributes}>'
);
```

Be sure you have set the URL to the root directory of your site in your config file or in `CP Home > Administration > General Configuration`.

Once you have that in place, you simply wrap the content you want to adjust. All images will be processed through Cloudinary.

```mustache
{exp:easy_cloudinary}
  YOUR CONTENT
{/exp:easy_cloudinary}
```

Any images (local or remote) will be swapped for Cloudinary-handled ones using the template you set up in the config file.

License
-------

Easy Cloudinary for ExpressionEngine is distributed under the liberal MIT License.