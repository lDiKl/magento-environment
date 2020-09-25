### Magento Commands List

#### Products 

    bin/magento indexer:info
    
    bin/magento indexer:status
    
    bin/magento indexer:reset
    
    bin/magento indexer:reindex

#### Modules

    bin/magento module:status
    
    bin/magento module:enable Vandor_Moudle --clear-static-content
    
    bin/magento module:disable Vandor_Moudle --clear-static-content
    
#### System 
    
    bin/magento setup:upgrade

    bin/magento maintenance:status
    bin/magento maintenance:enable
    bin/magento maintenance:disable

    bin/magento setup:uninstall

    bin/magento setup:di:compile
    bin/magento setup:static-content:deploy -f

    bin/magento deploy:mode:show
    bin/magento deploy:mode:set production / developer

    bin/magento config:set web/secure/base_url https://magento.local/
    bin/magento config:set web/unsecure/base_url https://magento.local/
        
#### Cache

    bin/magento cache:status
    
    bin/magento cache:disable config layout block_html collections reflection db_ddl compiled_config eav customer_notification config_integration config_integration_api google_product full_page config_webservice translate vertex
    bin/magento cache:enable config layout block_html collections reflection db_ddl compiled_config eav customer_notification config_integration config_integration_api google_product full_page config_webservice translate vertex

    bin/magento cache:clean && bin/magento cache:flush
    
    bin/grunt && bin/magento cache:enable config layout block_html collections reflection db_ddl compiled_config eav customer_notification config_integration config_integration_api google_product full_page config_webservice translate checkout

#### Regenerate Url rewrites

    bin/magento ok:urlrewrites:regenerate --entity-type=product
    bin/magento ok:urlrewrites:regenerate --entity-type=category

#### Cron 

    bin/magento cron:run
    bin/n98-magerun2 sys:cron:list
    bin/n98-magerun2 sys:cron:run cron_job
    
    
#### Admin 
    
    bin/magento admin:user:create --admin-user="admin" --admin-password="password" --admin-email="admin@mail.dev" --admin-firstname="Admin" --admin-lastname="Admin" 