# Data Management Using Business Manager Usage
[Return to Contents](README.md)

## Given a business requirement, modify site search preferences and settings to enable searching for a specified term or product attribute.
- **Search refinement definitions**
    - Determines which options can be used to refine search results
    - Options can include variation attributes like size and color
    - **Bucketing** allows for search options to be grouped together in "buckets"
        - Any number of buckets can be defined
- Configuring catalog level search refinement definitions
    - https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsearch_and_navigation%2Fb2c_configuring_catalog_level_search_refinement_definitions.html
- **Search Dictionaries**
    - Search dictionaries contain terms used to provide search results
    - These terms include:
        - Synonyms
        - Hypernyms
            - Words that describe a group of products
        - Hyponyms
            - Word that describes an item in the group defined by a hypernym
        - Common Phrases
            - Word combinations searched for together
        - Compound Words
            - Words that should be split into separate terms
        - Stop Words
            - Words ignored by search (an, the, etc.)
    - To add an entry to a search dictionary:
        - Navigate to site > Merchant Tools > Search Dictionaries
        - Select the dictionary type
        - Select "new" to create a new entry
        - Fill out the required fields, and save
- Setting up search dictionaries:
    - https://trailhead.salesforce.com/content/learn/modules/cc-einstein-smarter-search/cc-einstein-search-dictionaries
## Given a business requirement, create and configure a new search refinement and sorting definition that can be used on the storefront.
- Create new search refinements
    - https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsearch_and_navigation%2Fb2c_creating_new_search_refinement_definitions.html
- Additional search refinement documentation
    - https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsearch_and_navigation%2Fb2c_search_refinement.html
## Given a debugging requirement or code, configure the logging categories and access the logs in Business Manager.
- Configure custom log categories
    - https://documentation.b2c.commercecloud.salesforce.com/DOC2/index.jsp?topic=%2Fcom.demandware.dochelp%2FScriptProgramming%2FConfiguringCustomLoggingCategories.html
## Given business requirements, extend the storefront to expose a new attribute on an existing system object type.
- Business object documentation
    - https://trailhead.salesforce.com/content/learn/modules/cc-digital-for-developers/digital-business-objects
## Given a business need to store custom data, determine if a custom object is needed and create and configure as required.
- Whenever possible, use existing system objects to facilitate architecture upgrades
    - System objects can be extended to add additional attributes
- Creating a custom object
    - First create the custom object type, and define its attributes
    - Within the Manage Custom Objects module in business manager, enter the data for the custom object
- Business object documentation
    - https://trailhead.salesforce.com/content/learn/modules/cc-digital-for-developers/digital-business-objects
## Given a problem or performance issue and data, use relevant tools to inspect code performance and determine and implement solutions (cache configuration, profilers, etc) to resolve this issue.
## Given a specification and a sandbox instance, configure OCAPI permissions for Data and Shop APIs.
## Given a service configuration, recognize how they are applicable to the development process.