# How to update Wordpress Website

## Updating on Lightsail

## Notes

1. If you encounter any issues during the update you can check the Wordpress logs and the server logs for error messages
   Found in `/opt/bitnami/apps/wordpress/htdocs/wp-content/debug.log`
2. Verify updates done with `sudo wp plugin list` -> shows plugin names + versions

### 1. Backup the Website

It's crucial to backup your website before updating to be able to revert back to a working website.

### 2. Access Lightsail Instance

SSH into Lightsail Instance

### 3. Navigate to Your WP Directory

The default directory for WP on LS is usually
`/opt/bitnami/apps/wordpress/htdocs`

### 4. Disable Caching

It's a good idea to deactivate caching plugins to prevent any caching issues.

### 5. Update WP Code

`sudo /opt/bitnami/apps/wordpress/bnconfig --disable_banner 1` -> disables banner temporarily
`sudo wp core update` -> Updates WP Core

### 6. Update Themes and Plugins

`sudo wp theme update --all` -> Updates all Themes
`sudo wp plugin update --all` -> Updates all Plugins
`sudo wp plugin update dorito frito`-> Updates specified plugin by name of plugin; works with themes too

### 7. Enable Caching

### 8. Clear Browser Cache

Clear your browser cache to see the most updated version of your site

### 9. Test Website
