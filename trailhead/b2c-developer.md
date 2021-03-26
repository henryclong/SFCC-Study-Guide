# [Develop for Salesforce B2C Commerce](https://trailhead.salesforce.com/en/content/learn/trails/develop-for-commerce-cloud?trailmix_creator_id=strailhead&trail)
[Return to Contents](README.md)

## [Salesforce B2C Commerce for Developers](https://trailhead.salesforce.com/en/content/learn/modules/cc-digital-for-developers?trail_id=develop-for-commerce-cloud&trailmix_creator_id=strailhead)

### Get Started with Commerce Cloud Business Manager

- List three tasks a merchandiser performs in Business Manager.
    - Manage site-specific config settings and storefront data (products, catalogs, etc)
    - Configure search URLS and robots.txt
    - Review customer data and order details
- List three tasks a developer performs in Business Manager.
    - Create new sites
    - Troubleshoot problems.
    - Configure code versions
    - Register cartridges (containing code or data) with the server
    - Manage page cache settings
    - Set the site to online
    - Manage site taxation
    - Create custom error and maintenance pages to steer the shopper to what they want to buy
- List four tasks you can perform on the Administration tab.
    - Import and export site data
    - Move data/code to and from site instances
    - Manage customer lists and content libraries
    - Configure global settings such as
        - Locales and regional settings to support multiple languages
        - Password restrictions and login lockout policies for Business     - Manager users
        - Time zones
        - Order and customer sequence numbers
- Describe two features of the localization settings.
    - Business manager and the storefront can be localized differently
    - Locale preferences can be set by an admin user creating/editing a user profile, then by a user in their own profile settings

### Explore the B2C Commerce Development Environment

- List two tools used for the client portion of a Salesforce B2C Commerce storefront.
    - Templates
    - Form Definitions
    - Resource Bundles
- List the three key B2C Commerce software development tools.
    - Business Manager
    - Microsoft Visual Studio Code, 
    - Commerce Cloud Storefront Reference Architecture (SFRA)
- Describe the elements of the MVC architecture.
    - Model
        - Business logic, data, and underlying rules of the storefront
    - View
        - The storefront pages visible to a shopper
    - Controller
        - Takes input from entry fields and button clicks, and converts it into data and action to be consumed by the model or the view
- List three tasks you can perform with scripts and controllers.
    - Add calculations and logic to business processes
    - Call web services
    - Integrate back-end systems
    - Share information across users

### Explore the Commerce Cloud Storefront Reference Architecture

- Explain the benefits of using the Commerce Cloud Storefront Reference Architecture (SFRA).
    - Building sites is faster with out-of-box features
    - SFRA facilitates customization and overriding initial styles
- Explain why a reference architecture provides a blueprint for site design.
    - A reference architecture is a starting point for development, and includes best practices for design and architecture
- List two SFRA technical and UX components.
    - Controllers
        - Server-side scripts that handle requests
    - Cartridges
        - A bundle of code and/or data that is independently uploaded to a site
    - Bootstrap
        - Front end component library used to quickly build out a UI
- List two benefits of Mobile First.
    - Most customers access e-commerce sites via a mobile device
    - Designing for smaller screens is a good starting point for responsive design

### Explore B2C Commerce Business Objects

- Explain how business objects define the Salesforce B2C Commerce storefront data structure.
    - Business objects contain all of a store's data, compartmentalized into the appropriate objects
- List two reasons why you would customize system objects.
    - Default system objects are insufficient for the desired functionality
    - System objects are close enough in functionality to be altered, instead of replaced with a custom object
- List two reasons why you would use custom objects.
    - To more heavily customize store data
    - System objects cannot be customized to suit the desired functionality
- List the two business object best practices.
    - Use system objects instead of custom objects to facilitate SFRA upgrades and cut down on extraneous customization
    - Use system attributes instead of custom attributes whenever possible

## [Architecture of Salesforce B2C Commerce](https://trailhead.salesforce.com/en/content/learn/modules/architecture-of-commerce-cloud-digital?trail_id=develop-for-commerce-cloud&trailmix_creator_id=strailhead)

### Get Started Configuring Your B2C Commerce Sites

- List the instance types.
    - Sandbox
    - Staging
    - Development
    - Production
- Explain what the instance types are used for.
    - Sandbox
        - For development
    - Staging
        - Where changes are made before being pushed to development or production
    - Development
        - For testing changes made to staging
    - Production
        - The live storefront
- Describe how sites relate to organizations.
    - Multiple sites in an instance are grouped together in a single organization
- Describe how a multisite realm is managed.
    - Multiple sites within a realm can share a master catalog, share some admin settings, and be managed from different geographical locations

### Learn About Importing and Exporting Data

- Give two reasons why the import/export schema files are important.
    - Schemas standardize the structure of the data being imoprted/exported
    - Only data that matches the schema will be accepted
- List two types of data that are typically imported.
    - Product details
        - SKU numbers
        - Product descriptions
        - Sizes
        - Images
        - Prices
        - Video
    - Coupon codes
- Describe two import/export modes.
    - Merge
        - Update an object, or create an object if one does not already exist
    - Update
        - Update an existing object
    - Replace
        - Create a new object with the imported data
    - Delete
        - Remove an existing object
- Describe the export process.
    - Using business manager or a custom controller, export the database objects to an xml file
    - Transfer files from the instance to the merchant back end
    - Configure a secure connection if required for security compliance
- Explain why a delta feed is important.
    - Delta feeds contain only the changes from one export to another
    - These are smaller, which facilitates archiving, importing, and troubleshooting

###  Learn About B2C Commerce Replication

- Describe the process flow between instances.
    - A replication process is created in business manager
    - Multiple processes can be defined, each with different tasks
    - Schedule process time frame
    - Types of replication
        - Transfer
            - Transfers data between instances
        - Publish
            - Publishes transfered data
            - Published data must match transfered data
- List three types of data that are replicated.
    - Catalogs
    - Promotions
    - Coupons
    - Not:
        - Orders
        - Inventory lists
        - Business Manager profiles and logins
- List two differences between the import/export and replication processes.
    - Replication moves data between instances
    - Import/export moves data between B2C Commerce and external systems
- Describe two ways to control replication.
    - Specify which replication tasks to include
    - Specify the time fraame in which  to complete the replication
- Explain the benefit of replication tasks.
    - Replication facilitates data/code transfer between instances, and reduces any risk associated with import/export

## [Salesforce B2C Commerce Cartridges](https://trailhead.salesforce.com/en/content/learn/modules/b2c-cartridges?trail_id=develop-for-commerce-cloud&trailmix_creator_id=strailhead)

### Get to Know B2C Commerce Cartridges

- List three ways you can use a cartridge.
    - Controllers
    - Form definitions
    - Scripts
    - Static content (text, images, CSS files, and client-side JavaScript files)
    - Templates
    - Web Services Description Language (WSDL) files
    - Page Designer experiences (SFRA only)
- Explain why you need at least one custom cartridge to implement a storefront.
    - A custom cartridge is needed for customization, otherwise all that displays is the default SFRA storefront
- Describe where you can find the code version number.
    - `Administration > Site Development > Code Deployment` within business manager
- Explain the purpose of the cartridge path.
    - The cartridge path determines the precedence between cartridges. If a template is customized in two different cartridges, the one further left on the cartridge path will be used
    - This is in contrast to the cartridge stack, which just specifies the level of customization of a specific cartridge in relation to its peers

### Explore Reference Architecture Cartridges

- List what’s typically in a Storefront Reference Architecture (SFRA) cartridge stack.
    - Custom
        - Custom cartridges purpose built for a specific storefront
    - LINK
        - Cartridges built by LINK partnerst that integrate third-party functionality
    - Plugin
        - Integrates optional features to SFRA
    - Base
        - Core SFRA functionality
- Explain why it’s important to keep the SFRA base cartridges edit-free.
    - Keeping base cartridges edit-free facilitates smooth SFRA upgrades
- Classify the types of files in each base cartridge.
    - app_storefront_base
        - Contains the MVC models
    - bm_app_storefront_base
        - Contains files for Page Designer and business manager customization
    - modules
        - Contains objects that facilitate client server communication
- List what's typically in the cartridges folder.
    - Storefront_sg_controllers
        - Contains controllers, scripts, and templates for business processing
    - Storefront_sg_core
        - Contains templates and forms for the storefront UI
    - Storefront_sg_pipelines
        - Contains legacy pipelines and scripts for business processing

### Upload and Configure Cartridges

- Explain which tools you can use to upload Storefront Reference Architecture (SFRA).
    - dwpload
    - sgmf-scripts
- Explain the benefit of disabling page caching.
    - Disabling page caching lets developers see changes on the storefront without waiting for the cache to expire
- List three ways to view cartridges on the server.
    - Business Manager
    - Web URL
    - WebDAV
- Explain why rule-based storefront URLs should be disabled.
    - Rule-based storefront URLs may conflict with a default controller URL currently being worked on

### Customize Cartridges

- List three things you can do with sgmf scripts.
    - Upload a file to a sandbox.
    - Upload a cartridge.
    - Run tests on certain files or directories.
    - Compile css or js files.
    - Lint scss or js files.
    - Create a new cartridge structure.
- Describe how you can override the app_storefront_base cartridge.
- Explain how the global .scss file inherits styles.
- Describe how to include JavaScript modules from other cartridges.
