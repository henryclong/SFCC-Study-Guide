# Data Management Using Business Manager Usage
[Return to Contents](../README.md)

## Given a business requirement, modify site search preferences and settings to enable searching for a specified term or product attribute.
- **Search refinement definitions**
    - Determines which options can be used to refine search results
    - Options can include variation attributes like size and color
    - **Bucketing** allows for search options to be grouped together in "buckets"
        - Any number of buckets can be defined
- [Configuring catalog level search refinement definitions](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsearch_and_navigation%2Fb2c_configuring_catalog_level_search_refinement_definitions.html)
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
        - Navigate to `site > Merchant Tools > Search Dictionaries`
        - Select the dictionary type
        - Select "new" to create a new entry
        - Fill out the required fields, and save
- [Setting up search dictionaries](https://trailhead.salesforce.com/content/learn/modules/cc-einstein-smarter-search/cc-einstein-search-dictionaries)
## Given a business requirement, create and configure a new search refinement and sorting definition that can be used on the storefront.
- [Create new search refinements](https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsearch_and_navigation%2Fb2c_creating_new_search_refinement_definitions.html)
- [Additional search refinement documentation](https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsearch_and_navigation%2Fb2c_search_refinement.html)
## Given a debugging requirement or code, configure the logging categories and access the logs in Business Manager.
- [Configure custom log categories](https://documentation.b2c.commercecloud.salesforce.com/DOC2/index.jsp?topic=%2Fcom.demandware.dochelp%2FScriptProgramming%2FConfiguringCustomLoggingCategories.html)
## Given business requirements, extend the storefront to expose a new attribute on an existing system object type.
- [Business object documentation](https://trailhead.salesforce.com/content/learn/modules/cc-digital-for-developers/digital-business-objects)
## Given a business need to store custom data, determine if a custom object is needed and create and configure as required.
- Whenever possible, use existing system objects to facilitate architecture upgrades
    - System objects can be extended to add additional attributes
- Creating a custom object
    - First create the custom object type, and define its attributes
    - Within the Manage Custom Objects module in business manager, enter the data for the custom object
- [Business object documentation](https://trailhead.salesforce.com/content/learn/modules/cc-digital-for-developers/digital-business-objects)
## Given a problem or performance issue and data, use relevant tools to inspect code performance and determine and implement solutions (cache configuration, profilers, etc) to resolve this issue.
- Use the **Code Profiler** for insight into runtime performance
    - Can be found in `Administrator > Operations > Code Profiler` under the storefront to be profiled
    - Three modes:
        - Production Mode
            - Measures run-time behavior, provides an aggregated view
            - Default for non-sandbox environments
            - Cannot be disabled
            - Minimal performance impact
        - Development Mode
            - Measures run-time behavior, provides a detailed breakdown
            - Default for sandbox environments
            - Has some performance overhead
        - Extended script development mode
            - Same as development mode, and measures performance of script run-time behavior
            - Severe performance impact, not ideal for production
    - Results are flushed after changing modes
    - Code profiler data saved hourly into downloadable csv, followed by reset
    - Profiler only displays data since last reset
- [Use Code Profiler](https://documentation.b2c.commercecloud.salesforce.com/DOC2/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fgetting_started%2Fb2c_welcome.html)
- Cache
    - [Content Cache](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsite_development%2Fb2c_content_cache.html&resultof=%22%63%61%63%68%65%22%20%22%63%61%63%68%22%20%22%63%6f%6e%66%69%67%75%72%61%74%69%6f%6e%22%20%22%63%6f%6e%66%69%67%75%72%22%20)
    - [Configure the page cache](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsite_development%2Fb2c_configure_page_cache.html)

## Given a specification and a sandbox instance, configure OCAPI permissions for Data and Shop APIs.
- [OCAPI Settings](https://documentation.b2c.commercecloud.salesforce.com/DOC2/index.jsp?topic=%2Fcom.demandware.dochelp%2FOCAPI%2Fcurrent%2Fusage%2FOCAPISettings.html)
## Given a service configuration, recognize how they are applicable to the development process.
- **Web Service Configuration**
    - The Web Service Configuration manages timeout limits, failed call circuit breakers, and rate limits
- [Web Services](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fweb_services%2Fb2c_webservices.html)
- [Create a web service configuration](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fweb_services%2Fb2c_create_web_service_config.html)