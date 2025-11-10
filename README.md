# Skedulo Plus Examples

A set of example Skedulo Plus Mobile Extensions, to be deployed with the [Skedulo CLI](#Usage).

## Extensions

<table>
<tr>
  <!-- Hello World -->
  <td width="50%" valign="top">
    <h2>Hello World</h2>
    <img src="images/hello-world.jpg" alt="Hello World Extension" width="400"/>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A simple example with the bare minimum, displays some example text. This form doesn't require any customisation within Skedulo, and should be used as a base for creating new mobile extensions.</p>
      <b>Features</b><br/>
      <p>
        <code>Basic structure</code>, <code>Simple text display</code>, <code>Starter template</code>
      </p>
      <br/><br/>
    </details>
  </td>
  <!-- Account Details -->
  <td valign="top">
    <h2>Account Details</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A practical example that allows the user to view the attributes of an account related to a Job. This form can be easily extended to expose custom account fields as well as the <code>readonly</code> page flag can be removed to allow users to update the account fields displayed.</p>
      <b>Features</b><br/>
      <p>
        <code>Account viewing</code>, <code>Related records</code>, <code>Custom fields ready</code>
      </p>
      <br/><br/>
    </details>
  </td>
</tr>
<tr>
  <!-- Add Products -->
  <td width="50%" valign="top">
    <h2>Add Products</h2>
    <img src="images/add-product.jpg" alt="Add Products Extension" width="400"/> 
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A practical example that allows the user to view, edit and create Product records for use in the Job Products extension.</p>
      <b>Features</b><br/>
      <p>
        <code>CRUD operations</code>, <code>Product management</code>, <code>Form validation</code>
      </p>
      <br/><br/>
    </details>
  </td>
  <!-- Job Products -->
  <td valign="top">
    <h2>Job Products</h2>
    <img src="images/job-products.jpg" alt="Job Products Extension" width="400"/>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A practical example, allowing the user to view, edit and create Job Product records, and attach images. Requires Product records to be created using the "Add Products" or "Single Submission" extension.</p>
      <b>Features</b><br/>
      <p>
        <code>Job Products</code>, <code>Image attachments</code>, <code>List and detail views</code>
      </p>
      <br/><br/>
    </details>
  </td>
</tr>
<tr>
  <!-- Account Contacts -->
  <td width="50%" valign="top">
    <h2>Account Contacts</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A practical example, allowing a user to view, edit and create Contacts related to an Account for a given job.</p>
      <b>Features</b><br/>
      <p>
        <code>Contact management</code>, <code>Related records</code>, <code>Account relationships</code>
      </p>
      <br/><br/>
    </details>
  </td>
  <!-- Conditional Rendering -->
  <td valign="top">
    <h2>Conditional Rendering</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A version of the "Add Products" Extension with conditional rendering and dependant picklists. Demonstrates advanced form logic and field dependencies.</p>
      <b>Features</b><br/>
      <p>
        <code>Conditional fields</code>, <code>Dependent picklists</code>, <code>Dynamic forms</code>
      </p>
      <br/><br/>
    </details>
  </td>
</tr>
<tr>
  <!-- UI Components Showcase -->
  <td width="50%" valign="top">
    <h2>UI Components Showcase</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>An example containing all available components, intended only as a showcase to demonstrate the full range of UI components available for Mobile Extensions.</p>
      <b>Features</b><br/>
      <p>
        <code>All components</code>, <code>Reference guide</code>, <code>UI patterns</code>
      </p>
      <br/><br/>
    </details>
  </td>
  <!-- Read Only Extension -->
  <td valign="top">
    <h2>Read Only Extension</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A simple extension to display a read-only list of Product records. Useful for displaying data without allowing edits.</p>
      <b>Features</b><br/>
      <p>
        <code>Read-only views</code>, <code>Product listing</code>, <code>Display only</code>
      </p>
      <br/><br/>
    </details>
  </td>
</tr>
<tr>
  <!-- Single Submission Extension -->
  <td width="50%" valign="top">
    <h2>Single Submission Extension</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A simple extension to create Product records, does not allow for editing or listing. Ideal for quick data entry workflows.</p>
      <b>Features</b><br/>
      <p>
        <code>Single submission</code>, <code>Create only</code>, <code>Quick entry</code>
      </p>
      <br/><br/>
    </details>
  </td>
  <!-- Single Job Product Extension -->
  <td valign="top">
    <h2>Single Job Product Extension</h2>
    <br/>
    <br/>
    <details>
      <summary><b>ℹ️ More info </b></summary>
      <p>A simple extension to create a single Job Product per job, allows the record to be edited. Perfect for workflows requiring one product per job.</p>
      <b>Features</b><br/>
      <p>
        <code>Single record</code>, <code>Job Product</code>, <code>Edit capability</code>
      </p>
      <br/><br/>
    </details>
  </td>
</tr>
</table>

## Usage

These extensions are intended to be deployed with the Skedulo CLI.

In order to deploy them, you will need to log in to a tenant, this can be done with the following command

`sked tenant login web` or `sked tenant login token` if you wish to use an access token.

You will be prompted for your tenant name, and be asked if you wish to generate a long lived token.

### Deployment (create)

Run the following command to deploy the `HelloWorld` example to your tenant for the first time. Replace with value in `-f` with the appropriate folder if you wish to deploy a different extension.

`sked artifacts mobile-extension create -f HelloWorld.MobileExtension.json`

### Retrieval (get)

Run the following command to retireve the `HelloWorld` example from your tenant. Replace with value in `-o` with the folder you wish to store the extension in. Change the value of `--defId` to retrieve a different extension.

`sked artifacts mobile-extension get -o . --defId HelloWorld`

### Modifications (update)

Run the following command to update the `HelloWorld` mobile extension after you've made changes locally. Replace with value in `-f` and `--defId` with the appropriate folder and Definition ID if you wish to deploy a different extension.

`sked artifacts mobile-extension update --defId HelloWorld -f HelloWorld.MobileExtension.json`

### Deletion (delete)

Run the following command to delete the `HelloWorld`. Replace with value in `--defId` with the appropriate Definition Id if you wish to delete a different extension.

`sked artifacts mobile-extension delete --defId HelloWorld`

### Getting Help

Please see the [Mobile Extension documation](https://docs.skedulo.com/developer-guides/customize-and-extend-mobile/skedulo-plus-extensions/mex-intro/), and if you still experience issues please contact your Customer Success Manager.

