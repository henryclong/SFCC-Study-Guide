# Application Development
[Return to Contents](README.md)

## Given a development task, code ISML templates that use functionality such as: local include, remote include, components, and other ISML tags.
- ISML tag names are always prefixed with `is`
- Tags should be lower-case, although tag and attribute names are case-insensitive
- **Local Include**
    - Used when referencing a template
    - Can use a fixed value or expression in place of template name
    ```
    <isinclude template = template_name />
    ```
- **Remote Include**
    - Used when referencing content from a URL
    - Can use a fixed value or expression in place of URL
    ```
    <isinclude url = url_path />
    ```
- [ISML tag documentation](https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fisml%2Fb2c_isml.html)
## Use debugging best practices and techniques to troubleshoot scripts and controllers and verify outcomes.
## Given a requirement, create and extend the functionality of a JavaScript controller that leverages models, decorators, factories, or helpers following API best practices and renders a template or returns a JSON response.
- [Customize Templates (Decorator Templates in SFRA)](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_customizing_templates.html)
- [JavaScript Factory Functions with ES6+](https://medium.com/javascript-scene/javascript-factory-functions-with-es6-4d224591a8b1)
    - Factories are stored in the `cartridge/scripts/factories` directory
- Returning a JSON response from a controller
    - [11 Days: Playing with Templates (A JSON Response)](https://www.perimeterx.com/tech-blog/2020/11-days-of-salesforce-storefront-reference-architecture-sfra-day-11-playing-with-templates/)
## Given a business requirement and design for a new marketing page, develop page types and components to allow a marketer to build a page with the Page Designer tool.
## Given a requirement to accept, validate, and persist information from a storefront customer, modify the appearance of a form, add validation and CSRF protection, and use bindings to process fields.
- [Forms](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_forms.html&resultof=%22form%22%20)
    - [Creating a Form](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_create_form.html&resultof=%22%66%6f%72%6d%22%20)
    - [Validating Form Data](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_validate_form_data.html)
    - [Saving Form Data](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_save_form_data.html)
    - [Securing Forms (CSRF)](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_create_form.html)
- [Cross-Site Request Forgery (CSRF)](https://developer.salesforce.com/docs/atlas.en-us.pages.meta/pages/pages_security_tips_csrf.htm)
## Given localization requirements, implement and enhance templates, form definitions, static files, properties files, and persistent object attributes to ensure that pages are displayed in the expected language.
- Adding localized text using a properties file in the resources directory
    - [11 Days: Playing with Templates (Overcoming the Language Barrier)](https://www.perimeterx.com/tech-blog/2020/11-days-of-salesforce-storefront-reference-architecture-sfra-day-11-playing-with-templates/)
- [Form Localization](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_localizing_forms.html&resultof=%22%66%6f%72%6d%22%20)
## Given a logging task and existing configuration, write code that logs non-sensitive data to custom log files with different log levels.
## Integrate, deploy, and use a service instance based on a given requirement.
- Creating, initializing, and using a service
    - [11 Days: Using Services Framework](https://www.perimeterx.com/tech-blog/2020/11-days-of-salesforce-storefront-reference-architecture-sfra-day-6-using-services-framework/)
- Using services with URL paramaters
    - [11 Days: More Services Framework](https://www.perimeterx.com/tech-blog/2020/11-days-of-salesforce-storefront-reference-architecture-sfra-day-7-more-services-framework/)
## Given a use case, extend functionality or capture an event using hook extension points.
- [SFRA Hooks](https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsfra%2Fb2c_sfra_hooks.html&resultof=%22%68%6f%6f%6b%22%20)
> Hooks are executed in the order of the cartridges on the path.
- [OCAPI Hooks](https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2FOCAPI%2Fcurrent%2Fusage%2FHooks.html)
## Given code that violates documented best practices, identify the issues and modify the code to conform with best practices including performance and scalability.
## Given a business requirement, use OCAPI Shop and Data APIs to enable interoperability with an external system.
## Given a business requirement to perform a scheduled task, develop jobs and code job scripts.
- Creating a job, setting job steps, scheduling a job
    - [11 Days: Jobs](https://www.perimeterx.com/tech-blog/2020/11-days-of-salesforce-storefront-reference-architecture-sfra-day-9-jobs/)
- Creating a custom job script, interfacing a job with a service
    - [11 Days: Advanced Jobs](https://medium.com/perimeterx/11-days-of-salesforce-storefront-reference-architecture-sfra-day-10-advanced-jobs-d5b8a203ddba)