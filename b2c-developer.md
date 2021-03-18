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
- List three types of data that are replicated.
- List two differences between the import/export and replication processes.
- Describe two ways to control replication.
- Explain the benefit of replication tasks.
