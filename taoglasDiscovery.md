# Discovery: Taoglas Custom Object Creation

The goal here is to find out a way to create or update leads in HubSpot and asocciate a new record of a custom object called "Datasheet" to them since the download of a product datasheet from the Taoglas site on WordPress.


## Results

This is the process we found to solve this problem.

**1. Create a contact custom field called "Last datasheet downloaded"**

This custom field will allow us to save the product's datasheet URL in the contact properties and with this information proceed with the creation of the record of the custom object "Datasheet".

**2. Create a new HS form and embed it on WordPress sites**

Create a HS form to create or update contacts on HubSpot. This form will contain a hiden field with the URL of the product's datasheet. Also, this form is going to save this value in a custom field called "Last datasheet downloaded".

To find and to attached the product datasheet URL to the form will be a work performed by a FrontEnd developer with strong experience in WordPress.

**3. Create a contact-based workflow**

This workflow will be triggered by the creation or updating of a contact throught the form created in the first step. The main action will be a custom code that does the following:

- Check if this datasheet is already created.
    - If not, create the record with the product's datasheet.
    - If yes, continue with the following step.
- Associate this record with the contact involved.
- Associate this record with the contact's company.

### Possible issues

The main risk of this proposal is to have issues trying to get the produt datasheet URL in WordPress and send it hidden in the form.

This work will require strong and technical knowledge on WordPress and JavaScript to the developer be able to access this information and set it as a value in the form mentioned before.

## Platforms

WordPress

**Authorization:**

**FTP Credentials**

Accesible in the following ClickUp task: https://app.clickup.com/t/3fef9wm 

HubSpot

**Authorization:**

**Login info**

Accesible in the client's 1PassWord vault.
