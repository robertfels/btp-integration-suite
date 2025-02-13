<!-- loiob5968b260c1548418df4e529a9cb153f -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Manage Resources of an Integration Flow

Use *Resources* to manage different resources associated within an integration content optimally. The term "resources" refers to a collection of different categories of file types. A table in the resources view displays files grouped by categories and their filenames alphabetically sorted. Expanding each resource category shows the files within the category.

Resource files with a link allow you to view or modify the content in a file-specific editor. You can modify the file content only when the integration content is in edit mode.

> ### Note:  
> Mouseover the filename to view the access path.


<table>
<tr>
<th valign="top">

Category



</th>
<th valign="top">

File Type



</th>
<th valign="top">

Extensions



</th>
</tr>
<tr>
<td valign="top">

Archives



</td>
<td valign="top">

Archive



</td>
<td valign="top">

 `.jar` 



</td>
</tr>
<tr>
<td valign="top" rowspan="3">

Mappings



</td>
<td valign="top">

Message Mapping



</td>
<td valign="top">

 `.mmap` 



</td>
</tr>
<tr>
<td valign="top">

Operation Mapping



</td>
<td valign="top">

 `.opmap` 



</td>
</tr>
<tr>
<td valign="top">

XSLT Mapping



</td>
<td valign="top">

`.xslt`

`.xsl`



</td>
</tr>
<tr>
<td valign="top" rowspan="2">

Scripts



</td>
<td valign="top">

Groovy Script



</td>
<td valign="top">

`.gsh`

`.gy`

`.groovy`



</td>
</tr>
<tr>
<td valign="top">

Java Script



</td>
<td valign="top">

 `.js` 



</td>
</tr>
<tr>
<td valign="top" rowspan="3">

Schemas



</td>
<td valign="top">

XSD



</td>
<td valign="top">

 `.xsd` 



</td>
</tr>
<tr>
<td valign="top">

WSDL



</td>
<td valign="top">

 `.wsdl` 



</td>
</tr>
<tr>
<td valign="top">

EDMX



</td>
<td valign="top">

`.edmx`

`.xml`



</td>
</tr>
</table>



<a name="loiob5968b260c1548418df4e529a9cb153f__section_nbs_mvf_fbb"/>

## Adding Local Resources



### To add files from the file system, do the following:

You can add multiple resources from the file system. Also, archive the parent along with its dependent resources in a single `*.zip` file and add.

But you can't add multiple archive `(*.zip)` files or an archive file along with other resource files, only resources with the following extensions and dependencies are uploaded:


<table>
<tr>
<th valign="top">

Resource Type



</th>
<th valign="top">

Dependent Resources



</th>
<th valign="top">

You can...



</th>
</tr>
<tr>
<td valign="top">

WSDL



</td>
<td valign="top">

WSDL, XSD



</td>
<td valign="top">

Upload individual files or an archive file that contains multiple WSDL or XSD or both type resources.



</td>
</tr>
<tr>
<td valign="top">

XSD



</td>
<td valign="top">

XSD



</td>
<td valign="top">

Upload individual files or an archive file that contains only XSD resources.



</td>
</tr>
<tr>
<td valign="top">

EDMX



</td>
<td valign="top">

EDMX, XML



</td>
<td valign="top">

Upload individual EDMX or XML files, or an archive file that contains multiple EDMX or XML files or both type resources.

Ensure that your XML file contains the valid EDMX tag.



</td>
</tr>
<tr>
<td valign="top">

XSLT mapping



</td>
<td valign="top">

XSL



</td>
<td valign="top">

Upload individual files or an archive file that contains only XSL resources.



</td>
</tr>
</table>

> ### Note:  
> The resource view uploaders are supported for Remote APIs as well.

1.  In the *Local* tab, choose *Add* and select a file type.

2.  Select *File System* as the source.

3.  Choose *Browse* to select one or more files from the file system.

4.  Choose *Add* to upload the files.




### To add files from an integration flow project, do the following:

1.  In the *Local* tab, choose *Add* and select a file type.

2.  Select *Integration Flow* as the source.

3.  To import files from other integration projects, select the relevant *Package* and the *Integration Flow*s.

4.  In the *All Resources* table, select one or more files and choose *Add* to upload the files.

5.  To add dependent resources, select *Include Additional Resources*.

    > ### Note:  
    > MMAP files can be added from ESR. To know more, see: [Importing Mapping Content from ES Repository](importing-mapping-content-from-es-repository-e18fc05.md)
    > 
    > You can also copy MMAP files from other integration flows. While adding an MMAP file, the dependent resources get copied along with the file. You get to see a summary of the list of dependent resources in a dialog box before adding the file.

6.  In the *All Resources* table, select one or more dependent files and choose *Add* to upload the files.




<a name="loiob5968b260c1548418df4e529a9cb153f__section_trh_wxk_ctb"/>

## Referencing Resources

Apart from adding resources that are local your integration flow, you can also refer to reusable message mappings and script collections. You can refer to such artifacts from the package that you're in and other packages too. This way, when the reusable artifact is updated in the source, all referring integration flows are also automatically updated.

1.  In the *References* tab, choose *Add References* and select a reusable artifact type.

2.  Select one or more integration packages.

    You see a list of available reusable artifacts from the selected packages.

3.  In the *Artifacts* table, select one or more files.

4.  Choose *OK* to create reference for the selected reusable artifacts.




<a name="loiob5968b260c1548418df4e529a9cb153f__section_mnc_4dw_k1b"/>

## Quick Actions

You can perform the following actions for managing resource files:


<table>
<tr>
<th valign="top">

Actions



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

:wastebasket:



</td>
<td valign="top">

Removes relevant resource file from the integration flow. Before deleting make sure that the selected file isn't being referred in other integration flows.



</td>
</tr>
<tr>
<td valign="top">

<span class="SAP-icons"></span> \(Download\)

\(Applicable only for local resources\)



</td>
<td valign="top">

Downloads the respective resource file to your local file system.

> ### Note:  
> While downloading an MMAP file, all dependent resources get downloaded along with the file in a ZIP format.
> 
> Read the [blog](https://blogs.sap.com/2020/03/02/sap-cloud-platform-integration-download-and-upload-of-message-mapping/) and know more about download and upload of Message Mapping.



</td>
</tr>
</table>

