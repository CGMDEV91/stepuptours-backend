# stepuptours-backend


## clean installation
````
ddev drush sql-drop -y
ddev drush site-install \
    --site-name="StepUp Tours" \
    --site-mail="admin@admin.com" \
    --account-name="admin" \
    --account-pass="admin" -y

ddev drush config-set 'system.site' uuid e6b2cad2-8cbe-4775-8780-6b2ed846c349 -y
ddev drush cr
ddev drush ev '\Drupal::entityTypeManager()->getStorage("shortcut_set")->load("default")->delete();'
ddev composer install
ddev drush cr
ddev drush cim -y
````
