---
sidebar_position: 1
---

# Manage Docs Versions

Docusaurus can manage multiple versions of your docs.

## Create a docs version

- The ticket starts at IN ANALYSIS
- Create a new branch per feature. For example YOUR_NAME/TAS-3395
- When the development is done, ensure to update any API documentation and monitoring dashboards if needed. push your branch to Github and create a Pull Request to the UAT branch, assign code reviewers viet.nguyen3 and trung.nguyenbao.
- Move the ticket to READY FOR CODE REVIEW.
- Code reviewers will move the ticket to IN CODE REVIEW, Fix any code review issues.
- When code review is done, move it to READY FOR FEATURE TEST and QC will take care of testing the ticket in the UAT environment and moving the ticket forward accordingly.
- When QC find a bug, they will create a new ticket, link it to the original ticket and add it to IN ANALYSIS. They will assign the backend engineer to it.
- When the ticket is in READY FOR RC TEST, create a pull request to the production branch and assign viet.nguyen3 and trung.nguyenbao as code reviewers
- When code review is done and merge is complete. Contact Mohammed (SDM) with the Pull Request for your code to be released.

## Add a Version Dropdown

To navigate seamlessly across versions, add a version dropdown.

Modify the `docusaurus.config.js` file:

```js title="docusaurus.config.js"
module.exports = {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: 'docsVersionDropdown',
        },
        // highlight-end
      ],
    },
  },
};
```

