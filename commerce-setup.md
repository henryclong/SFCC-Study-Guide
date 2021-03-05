# B2C Commerce Setup
[Return to Contents](README.md)

## Given a sandbox environment, configure an IDE to use WebDAV to deploy cartridges to the correct version directories.
- Using [dwupload](https://www.npmjs.com/package/dwupload)
  - Install dwupload via npm
  - Create dw.json at the project root, and fill out the following:
    - hostname
    - username
    - password
    - code-version
    - Sample dw.json:
      ```json
      {
        "hostname": "sandbox-01-inside-the-realm.cloudkicks.net",
        "username": "vlahiri",
        "password": "yourpwd",
        "code-version": "version1"
      }
      ```
  - Use the dwupload command to upload the cartridge. Command line arguments will override the config file values
- Using [sgmf-scripts](https://www.npmjs.com/package/sgmf-scripts)
  - Install sgmf-scripts via npm
  - Use the sgmf-scripts `--createCartridge` command to create the dw.json file
  - Use the sgmf-scripts `--uploadCartridge` command to upload the cartridge
- Additional Resources
  - [Upload and Configure Cartridges Unit | Salesforce Trailhead](https://trailhead.salesforce.com/content/learn/modules/b2c-cartridges/b2c-cartridges-upload-configure)
  - [Using WebDAV | Salesforce Commerce Cloud Infocenter](https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fimport_export%2Fb2c_using_web_dav.html)
  - [Access WebDAV Files | Salesforce Commerce Cloud Infocenter](https://documentation.b2c.commercecloud.salesforce.com/DOC3/index.jsp?topic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fadmin%2Fb2c_access_files_webdav.html)

## Given a sandbox instance and data import files, import files using the Business Manager Import/Export modules.
- Additional Resources
  - [Explore Business Manager Import and Export Unit | Salesforce Trailhead](https://trailhead.salesforce.com/content/learn/modules/b2c-import-export/b2c-business-manager-import-export)
## Given the code for a storefront site, add the correct sequence of cartridge names to the provided cartridge path.
## Given a sandbox environment, use the Business Manager to add a new site to the instance, configuring the default currency and taxation type according to business requirements.
- [Get Started with Commerce Cloud Business Manager Unit \| Salesforce](https://trailhead.salesforce.com/content/learn/modules/cc-digital-for-developers/cc-business-manager)
## Given a recently created B2C site, assign the storefront data configurations according to business requirements.
- [Review Business Manager Settings Unit \| Salesforce Trailhead](https://trailhead.salesforce.com/content/learn/modules/b2c-solution-functional-launch-readiness/b2c-review-business-manager?trail_id=apply-a-salesforce-b2c-commerce-functional-solution)