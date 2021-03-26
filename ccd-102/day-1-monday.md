# Day 1 - Monday
[Return to Contents](../README.md)

- General Notes
  - 1 Month of sandbox access
  - Will provide cert advice at end
  - Sandbox Number is `045`
  - Actual API is Java
    - JS is running on JRE(?)  in a ruby interpreter
    - No programming actually happens in Java
  - Make sure node version `4.0 =<  version < 12.0.0` for CLI exercises
- Salesforce B2C Commerce Integrations
  - B2C Commerce is not the source if truth for product inventory
- Instances
- B2C Commerce Infrastructure
  - POD: Point of Delivery
    - Salesforce owned, in third party data centers
  - Realm: Within POD
    - Cannot communicate directtly with each other
    - Must import/export
    - PIG: Primary Instance Group
      - Development, Staging, Production
      - Code typically not transferred directly from sandbox to staging
        - Typically stored in and pushed from VCS
    - SIG: Secondary Instance Group
      - Realm Sandboxes
      - Demo Sandbox
        - Automatically wiped and reloaded every release with a fresh copy of Site Genesis and SFRA
        - Can always compare with a vanilla version of the code, in case of bugs on a sandbox
        - Can be used for initial integration testing (before staging), but should be temporary
  - Typically 8-16 releases a year, never in the fourth quarter
- Storefront Reference Architecture (SFRA)
  - OOB Blueprint
- SFRA Cartridge Stack
  - Whenever possible, go through SFRA
  - Can alter SFRA core codebase, but shouldn't if at all possible
    - Salesforce will not help with issues arising from this
  - If multiple sites share branding, separate common functionality and site specific functionality
- Model View Controller (MVC) Architectural Pattern
  - Promotes modular and maintainable coe
  - Pattern, not requirement
- Business Manager
  - 15 minute inactivity timeout for login
    - For PCI Compliance
    - BM doesn't know if BM is connected to a Sandbox or Production
  - DWithEase (Demandware with Ease)  
    - Not officially recommended
    - Used to bypass logout timer
    - Only use in sandbox, bypassing 15min logout violates PCI
  - Sandboxes are white on black, prod is red
- Knowledge Check
  - Name the architectural pattern of SFRA
    - MVC
  - Two BM features
    - Import/export data, update products, update content slots
- Break
- 2-1: Access SFRA
  - Typically site imports only import data
  - SFRA import is unique in that it imports data + code
- Storefront & Master Catalog Structure
  - Each storefront has
    - One or more master catalogs
    - One storefront catalog
      - Defines the navigation for the site
- 2-2: Share catalog data between sites
  - ids are case sensitive
  - New site name will appear in URL, encoded (%20 for spaces)
  - Changes will not be posted until `apply` button is pressed
    - Salesforce screens will give warning if there are unsaved changes
    - Demandware screens will not display a warning
  - Brand new site will have the demandware base code if nothing else is deployed (green background with salesforce logo)
  - Categories in storefront catalog define site navigation
    - Categories are actually `Search-Show?gid=CATEGORY_ID`
    - Empty categories do not appear in navigation
      - Empty search does not generate category page
- 2-4
- Knowledge Check
  - SFRA code can be accessed through Github
    - True
  - You do not need to rebuild search indexes for a site
    - False
- Cartridge
  - What is a cartridge?
    - A folder with a set of resources
  - Provides specific storefront features or integrations
  - Has specific subfolders for different types of resources
- Cartridge Directory Structure
  - Compiled/minified js/scss is sent to `static` directory
  - No sub directories in `controllers` directory
  - Any JS that isn't a controller or model goes in the scripts folder
    - Helpers, etc.
- Cartridge Path
  - Determines what gets executed in what order
- Cartridge Execution
  - Cartridges are prioritized in left to right order
- Cartridge Path COnsiderations
  - Plugins are developed against the base cart, not each other
    - May contain conflicting code
      - `plugin_catrdridge_merge` handles conflicts between plugin cartridges
      - Included by default in all-in-one code base from BM
      - Unlikely to happen in LINK carts, but may
        - Try to use unique name spaces
- SFRA Modules
  - Uses CommonJS for common functionality
- 3-1: Work with Plugin Cartridges
  - lib_productlist is required for wishlist and gift registry plugins
  - To uninstall a plugin (such as wishlist) disable it in the custom preferences and remove it from the cartridge path
- 3-3: Create a New Code Version
  - For dw.json password, use WebDAV access key instead of actual password
  - To upload catrridges with pro
    - `Prophet (Cloud Icon) > More Actions... > Prophet: Enable Upload`
- Knowledge Check
  - What are the two main directories you'll  find in the SFRA
    - Modules
  - Why is the order of the cartridges on the cartridge path
important?
    - Determines the precedence of functionality
- Controller
  - Server side script that handles requests
  - Manages data flow in application
  - Written in JS and B2C commerce script
- B2C Commerce  Script
  - Based on JS
    - Used in controllers and ISML Templates
      - Not recommended  to use directly in template
  - When one says "B2C Commerce Script", it means a script that accesses the API
- require paths
  - `~/` Look in root of cart
  - `*/` Look in cartridge path
  - `./` Look in current directory
  - `../` Look in parent directory
  - `dw/` Look in scripts API
  - `server` get server object
- Server Module
  - Every controller must end with `next();`
    - Controllers are middleware, next calls next function in chain
    - Can also pass along errors with `next(new Error())`
- Types of routes
  - `server.use` responds to both `GET` and `POST` requests
    - Not found in base cart
- Add Middleware Functions
  - `req`
    - Used when looking for input information
  - `res`
    - Used for outputting information
  - `next`
    - Calls next function in chain
- 4-1
  - Pipeline not found error
    - Indicates that controller was not found, so SFRA looked for pipeline (which was also not found)
- Passing parameters
  - res.render() has two arguments
    - Template
    - Parameters to pass into pdict
  - `${}` Indicates an expression, with the contents of the braces being evaluated
- Troubleshooting
  - Ensure cartridge directories are within the `cartridges` directory 
    - This is where prophet will expect to find them
  - Ensure local code version matches live code version
  - Cartridge path names are case sensitive
  - Check cache settings, ensure it's disabled
  - Check indexes
  - Make sure that all files are saved and uploaded
- 4-3
  - Request Log
    - Under `toolkit` in BM
    - `Clear` does not clear entire request log, only what is currently displayed on the page
- 4-4
- superModule
  - Allows for extending of javascript modules
  - References the same module in a different cartridge
    - Cartridge is the next cart to the right on the cart path
  - This is how multiple controllers can run code on the same request (middleware)
  - superModule options
    - append
      - Inserts functionality after original functionality
    - prepend
      - Inserts functionality before original functionality
    - replace
      - Completely replaces original middleware
- 4-6
  - If using `res.getViewData()`, `res.setViewData()` is not required
    - viewData is passed by referenced
  - `setViewData()` appends viewData, it does not replace the object
- 4-7
- B2C Commerce Script API
  - Sandboxes updated at least two weeks before PIG instances
  - Updated documentation included with update
  - Version number included in BM
  - Can set site for earlier version compatibility if not using current features
- B2C Commerce API Packages
  - Two types
    - Storefront
      - Has to do with campaigns, catalogs, orders
    - Background
      - Behind the scenes
- Product Factories
  - Access API through models instead of directly