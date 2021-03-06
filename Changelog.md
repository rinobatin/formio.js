# Change Log
All notable changes to this project will be documented in this file

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## 3.9.0
### Added
 - FOR-1787: Ability to save Day component with empty day / month / year, added trailing zeros to saved value
 - Added File types
 
### Fixed
 - FOR-1850: Wrong key for Encrypted setting in builder
 - FOR-1847: Renderer crashing when TextArea is rendered in readOnly and viewAsHtml mode
 - FOR-1779: Fixed issues with multiple errors showing up on wizards.
 - Possibility to hide PDF submit button.

## 3.8.0
### Added
 - Added the CKEditor WYSIWYG available for textarea editors.
 - FOR-1758: Allow for another option of persistence called "client-only" which won't send the data to the server.

### Changed
 - Changed the Content building to use CKEditor.

### Fixed
 - FOR-1845: Builder buttons missing for components with Logic
 - Hide "edit" and "delete" on readOnly for EditGrid
 - Button was disabled while it shouldn't be for Read Only forms, or when configured to always be enabled.

## 3.7.0
### Changed
 - Added the 'hideOnChildrenHidden' parameter for Columns to hide when their children are hidden.
 
### Added
 - FOR-1806: languageChanged event
 - FOR-1844: Support for private file downloads with the URL file configuration. Also added a File Upload server @ https://github.com/formio/formio-upload that supports this feature.
 
### Fixed
 - FOR-1595: Placement of description for Edit Grid
 - FOR-1657: Select component Values template.
 - Fix bug with widget field being displayed on TextArea and Password
 - FOR-1816: DateTime -> Unchecking '12 Hour Time (AM/PM)' checkbox not changing date format automatically
 - FOR-1815: Time component for Safari
 - FOR-1688, FOR-1508: Tabs component issues when building.
 - FOR-1398: Make columns component adjust on each render

## 3.6.13
### Fixed
 - FOR-1821: Number component min and max validation.
 - FOR-1731: Fix bug with Content component in Wizard builder.
 - FOR-1728: Fixed more issues around text masks and iOS browsers.
 - FOR-1646: Blur events are forcing the select dropdowns to close.
 - FOR-1647: Checkboxes are not getting set in the correct default states.

### Changed
 - Upgraded moment-timezone@0.5.23

## 3.6.12
### Fixed
 - FOR-1745: Children components context for Container, DataGrid and EditGrid component.
 - Make sidebar buttons work after adding component.

### Added
 - FOR-1757: Content property to HTML and Content components Logic.

### Changed
 - Upgraded webpack@4.23.1, eslint@5.8.0, i18next@12.0.0

## 3.6.11
### Changed
 - Export the "moment" object in FormioUtils so that it can be accessed from outside libraries.

## 3.6.10
### Fixed
 - FOR-1491: Fix bug with Day when form rendered as HTML 
 - FOR-1812: Fixed issues where timezones were not converting properly.

## 3.6.9
### Fixed
 - FOR-1747: Fixed many issues related to contextual data getting swapped (row vs. data) for certain checks within the renderer.
 - Issues where error messages for fields would get drowned out (color-wise) when errors are showing up per-field.

## 3.6.8
### Fixed
 - FOR-1793: Fixed an issue where a "/" would be appended to the Day component value when "Hide Year" was checked.
 - Fixed a small bug where components may disable when they are not supposed to be.
 - Problems where the highlighted errors and custom errors would not persist when they are presented.
 - FOR-1789: Fixed an error where day component would cause beta portal to show 'Cannot read property data of undefined' in data section.

### Changed
 - Upgrade gulp-sass@4.0.2, i18next@11.10.0, eslint@5.7.0, webpack@4.21.0

## 3.6.7
### Fixed
 - Problems with the Select component not working with Refresh On property for some cases.

## 3.6.6
### Fixed
 - FOR-1733: Fixed issue with preview destroy on change.
 - FOR-1728: Problems with running the renderer within iOS applications.
 
## 3.6.5
### Fixed
 - Broken build.

## 3.6.4
### Chanded
 - FOR-1591: API key regex.

### Fixed
 - FOR-1756: Number component missing delimiters when rendered in Edit Grid
 - Allow webcam to upload at a higher resolution.

### Added
 - FOR-1762: 'wizardNavigationClicked' event for case of Wizard's top navigation click

## 3.6.3
### Fixed
 - FOR-1614: Configure the textfield calendar widget to store date as text without timezone conversion.
 - FOR-1489: Make sure to alter the Date format according to which settings they have enabled/disabled. For Enable Time, Enable Date, and 24hr time.
 - FOR-1754: Fixed problems where the calculateValues would not get fired when navigating between tabs.
 - FOR-1755: Infinite onChange events being fired when editing a component in the builder.
 - FOR-1636: Fixed when you check the 'Disabled' setting for component, you are unable to set the default value as the setting disables the Default value field
 - FOR-1587: Issues where the remove select item button is visible when component is disabled.
 - FOR-1733: Problems where the calendar would not properly destroy.
 - FOR-1733: Issues where the component preview would not properly destroy.

### Added
 - FOR-1637: Ability to manually override calculated values.
 - FOR-1558: Tests to ensure there is not an issue with setting submissions with containers.

### Changed
 - Upgrade @babel/cli@7.1.2, @babel/core@7.1.2, eslint@5.6.1, sinon@6.3.5
 - Moving the Form utilities to their own separate files.

### Fixed
 - Custom validation of components inside EditGrid.

## 3.6.2
### Fixed
 - Fixed problems with infinite onChange events when hiding a multi select component with clearOnHide enabled.

## 3.6.1
### Fixed
 - FOR-1693: Fixed data grid setValue to refresh rows when value changes.
 - FOR-1691: Ensure the DateTime widget is disabled when the component is disabled.
 - FOR-1507: Fixed an issue where the 'disableOnInvalid' flag for buttons would not work for forms that are in a pristine state.
 - Fixed issues where infinite onChange event would happen for conditionally hidden elements with clearOnHide + multiple configurations checked.
 - FOR-1718: Fixed the initialization events to be more deterministic. Also added an 'initialized' event after everyting is done initializing.

## 3.6.0
### Added
 - FOR-1732: Ability to have buttons in builder sidebar.

### Fixed
 - FOR-1705: HTML Element and Content Components losing content when any Logic is applied,
 - FOR-1705: moved 'customClass' CSS class from HTML content wrapper to regular formio component wrapper
 - FOR-1706: Added 'CSS Class' (className) builder setting for Content component which adds
 - FOR-1700: Issues with IE11 by introducing polyfills.
 - FOR-1497: Initial focus on HTML5 Select component.
 - FOR-1709: Conditionals for Form component.
 - FOR-1681: Token issue for iframe.
 - Fixed issue where externally bound events would get removed during redraw events.
 - Fixed the wizard builder page labels to be the correct colors.
 - Issues with the Inline embed codes not working with browser updates.

## 3.5.7
### Fixed
 - Prefix and Suffix for Bootstrap 4.

## 3.5.6
### Fixed
 - FOR-1566: Select component to use `asString` so it will show the label instead of the value.
 - FOR-1659: Form Builder preventing removing values from JS code fields (fixed Ace Textarea not firing onChange event when empty)
 - FOR-1659: Fixed Ace Textarea not firing onChange event when it gets empty

### Added
 - FOR-1599: Ability to change CSS Classes using Logic
 - FOR-1717: A class of formio-component-multiple for fields with multiple configurations.

## 3.5.5
### Fixed
 - Downgrade whatwg-fetch to 2.0.4 so that this library can be used in node.js without an error being thrown.

## 3.5.4
### Fixed
 - FOR-1712: Make sure that an empty time component does not trigger infinite onChange events.
 - FOR-1711: Ensure that the builder does not execute conditionally hidden elements.
 - FOR-1701: Fix empty check for datetime component which can be a data object.
 - FOR-1287: Move field logic event trigger to build so context is set correctly and interpolate event so it will work with rowIndex.
 - The styles for the phone number component with locale configurations for Bootstrap 4.

### Added
 - FOR-1663: Added collapsible and collapsed to the Panel and also added icon to show collapsed state.

## 3.5.3
### Fixed
 - FOR-1586: Survery component input names.
 - FOR-1363: Fixed issue where validations would fire twice when a button component is present.
 - FOR-1650: Fixed problem where multiple "change" events would fire on form render.
 - FOR-1581, FOR-1582: Fixed issues with Signature component would get in a bad state when conditional logic is applied."
 - Problem where an error would get thrown for NumberComponent and "decimalSeperator" references.

## 3.5.2
### Fixed
 - FOR-1675: Textarea not displaying whole its content in readOnly mode
 - FOR-1417: Caching logic to return promises instead of resolved responses.
 - Fixed problem where nested components would fire calculate value of children when it is conditionally hidden.
 - FOR-1673: Problem where the refreshOn would only trigger first time.
 - FOR-1389: Issue where you could not upload another file when one is removed.

### Added
 - FOR-672: Add uiquify step to copyComponent method.

### Changed
 - Update lodash@4.17.11, @babel/core@7.0.1, i18next@11.9.0, sinon@6.3.2, webpack@4.19.0, whatwg-fetch@3.0.0

## 3.5.1
### Fixed
 - Issues where the PDF builder would not load.

## 3.5.0
### Fixed
 - Problem where icon configurations would not get passed to sub forms.
 - Issue when building tabs, they would reset to first tab.
 - Adding data to add components when moving between tabs.
 - Fixed a problem where clearOnHide would trigger when navigating between tabs.
 - Fixed problem where extending forms would modify the Base forms.
 - Panel style themes for Bootstrap 4 to be consistent with Bootstrap 3.
 - Issue where the builder would resize continuously.

### Changed
 - Hide the label settings for Panels since they have a title field.
 - Upgrade to Babel 8.0 compilations.
 - Upgraded demo application to Bootstrap 4.
 - Default size for EditGrid buttons to small.

### Added
 - URL component
 - Ability to provide global icons using Formio.icons property.

## 3.4.8
### Fixed
 - Problems where the builder sidebar would not collapse the first group causing style issues.
 - FOR-1618: Fixed problems with infinite refresh loops when clearOnHide is used.
 - FOR-1670: Fixed issue in EditGrid where errors would persist and not get cleared when a row is canceled.
 - FOR-1665: Fixed issues where default hidden states would not be set for nested conditionals.
 - Clear errors when components are hidden.

### Added
 - Option that adds the ability to add primary project id to the pdf download icon.
 - A 'change' event to the webform builder anytime the schema changes.

## 3.4.6, 3.4.7
### Fixed
 - Cosmetic changes with Bootstrap 4
 - Fix namespacing of user tokens.

### Changed
 - i18next@11.7.0, sinon@6.2.0

## 3.4.5
### Fixed
 - Issues with the setHidden not working since they were not added to containers.

### Changed
 - Upgrade flatpickr@4.5.2, ace@1.4.1

## 3.4.4
### Added
 - Better settings for webcam and make it initialize properly when switching modes.

### Fixed
 - The form builder to hide sections when the others are clicked for Bootstrap 4.
 - The form builder to show the default section at first.
 - The signature refresh button to use the correct class for bootstrap 4.
 - Style problem where hidden labels would add a space to the top of the control.

## 3.4.3
### Fixed
 - Issues where sessionStorage was making the renderer crash for IE browsers.
 - Problems with the ContainerComponent where it would reset the data objects and stop tracking data changes.
 - Problem with the core renderer to work when it is pointing to the Form Action API.
 - Fix web camera option for image uploads.

## 3.4.2
### Fixed
 - Field logic simple conditional when key.

## 3.4.1
### Added
 - FOR-1635: Add button for taking picture with webcam to image file components.

### Fixed
 - FOR-1644: Required marks missing when Hide Label is checked for a component
 - Field logic simple conditional and set required not setting properly.
 - FOR-1618: Fix infinite loop with hidden, clearOnHide and calculateValue.
 - FOR-1645: Fix columns in datagrids disappearing.

## 3.4.0
### Added
 - FOR-1614: Concept of input "widgets" which allows you to attach "calendar" to TextField. More to come.
 - FOR-1614: Widget settings to TextField component.

### Changed
 - FOR-1616, FOR-1615: Make sure the calendar enforces an input mask and also updates the date on a blur event of the input.

### Fixed
 - Make sure to not send an invalid API call when no resource is provided.
 - Make the select component work when project url is provided.
 - Fixed the select component to trigger a refresh when visibility changes.
 - Fixed the ACE editor to not trigger infinite refresh when new value and existing values are both empty.
 - FOR-1618: Fix bug where select could get in infinite change.

### Removed
 - FOR-1579: Settings from DateTime component that no longer apply to core renderer.

## 3.3.7
### Fixed
 - Problems with infinite onChange events firing from SelectBoxes component.
 - FOR-1500: Error messages displaying.
 - FOR-1500: OnChange event infinite loop on Wizard.
 - Error from occurring in the TextArea builder modal.
 - WYSIWYG: being empty in read only mode in Wizard on non-first page
 - FOR-1604: Fixed issue where Select with RefreshOn + ClearOnRefresh will clear its value even when its refresh dependency does not change values.
 - Issues with EditGrid triggering validation preemptively.

### Added
 - Edit Grid: 'formio-component-editgrid-row-open' class for case when any row is open
 - FOR-672: Copy and paste features on the builder.

## 3.3.6
### Fixed
 - Issues with the embed script to try and grab wrong script from the page.
 - Problems where the default embed script is in Webpack develop mode.

## 3.3.5
### Fixed
 - Path issues with s3 uploads that was adding empty directories to the upload paths.

## 3.3.4
### Fixed
 - Issues with Invalid date showing up for display times in UTC.

### Changed
 - Minor text change for the form builder.

## 3.3.3
### Fixed
 - Issue where the Content component would not work in builder with Refresh on Change checked.

## 3.3.2
### Fixed
 - Problems with undefined promise if no timezone is used.
 - Default datetime component to now show 24 hour time.
 - Fixed placeholder on DateTime component to show the standard form.io time format.

### Changed
 - Added help docs to the DateTime component.

## 3.3.1
### Fixed
 - FOR-1560: Date timezones to use moment-timezone with lazy loading zones.
 - FOR-1445: Problems where duplicates could show up in Select component
 - Issue that arrises when you send a malformed language code to the switch language system.
 - Added try/catch blocks around language switching to make it so the renderer is still usable.

## 3.3.0
### Added
 - A DataMap component that provides a dynamic key-value pair input component.

 ## Changed
  - Cleanup code around setting the locale in the DateTime component.

### Fixed
 - FOR-1570: Fixed an issue where the validation would not be removed if the form is valid.
 - FOR-1549: Fixed a problem with Properties settings in form builder was giving wrong format. Changed to DataMap component.
 - FOR-1326: Fixed an issue where a language change would not re-trigger conditionals.

## 3.2.3
### Fixed
 - Datetime component crashing when using locale format.

## 3.2.2
### Fixed
 - Issue where the timezone dropdown was not showing up on DateTime component.

## 3.2.1
### Added
 - Allow for global overrides of components and let the form.settings override components globally.
 - Allow for custom timezones for the DateTime component.
 - Save the "path" and "options" in Formio class so that they can be passed along to other instances.
 - FOR-1542: Update `build` method of `Container` component.

### Fixed
 - The acronym for offset 0 time is GST not GMT.
 - Fix issue where select and radio components end up in an infinite refresh when hidden with "clearOnHide" set.

### Changed
 - Moved timezone formatting to utils so that it can be used in templates.

## 3.2.0
### Added
 - A way to track submission metadata including referrer, timezone, etc.
 - An option to view the DateTime component in either the Viewer, Submission, or GMT timezones
 - A tableView method to show the data in a submission grid correctly.
 - A method for working with Encrypted S3 buckets.
 - A way to configure the Columns component so that it hides columns where all elements are hidden in that column.
 - A different view widget to view images with file component on devices that support Camera.
 - A way to input text into the DateTime component.
### Changed
 - Upgraded i18next@11.6.0 and upgraded dev dependencies.
### Fixed
 - Tooltip options to make them behave better.
 - Protect calls to getAllComponents where it was sometimes on null.

## 3.1.4
### Added
 - Emitting Edit Grid event for row addition
### Fixed
 - Edit Grid not firing outer calculations on 'Save' button click
 - Problem with DataGrid where its value would not be correct when there were Panels within the DataGrid.

## 3.1.3
### Fixed
 - Problem with the PDFBuilder component where it would remove listeners for the drag-and-drop components.

## 3.1.2
### Fixed
 - The styles for checkbox so that it will look good for both radio and checkboxes.

## 3.1.1
### Fixed
 - An issue where EditGrid may not default to show its values.
 - The readonly view of EditGrid to now show add and remove buttons.

## 3.1.0
### Added
 - Minimum search setting for Select component that would hold off on sending API until they type a certain length.
 - Adding submission to the evalContext so you can do things like {{ submission.created }} in templates.
 - Add validation check to edit form on builder.

### Changed
 - Upgrade text-mask-addon@3.8.0

### Fixed
 - WYSIWYG issue with cursor jumping in the beginning of line on setValue
 - Fixed issue with EditGrid validating and adding rows in the correct order.
 - Fixing DataGrid to not trigger infinite update loops.
 - Making DateTime not trigger constant update handlers.
 - Fixed the Radio component to also check for undefined values.
 - Fixed issue with the builder resetting the sidebar when items are added.
 - Fixed empty single select rendering improperly

### 3.0.0
#### Breaking Changes
 - Changed the overrall structure of the library and how "imports" work to make them more structured.

    ```js
    // To render a new form.
    import { Form } from 'formiojs';
    const renderer = new Form(document.getElementById('formio'), 'https://examples.form.io/example');
    renderer.render();
    ```

    ```js
    // To render a form builder
    import { FormBuilder } from 'formiojs';
    const builder = new FormBuilder(document.getElementById('builder'), {components:[]});
    builder.render();
    ```

    ```js
    // To import a component
    import TextFieldComponent from 'formiojs/components/textfield/TextField';
    ```

 - Changed FormioComponents name to NestedComponent.
 - Changed FormioComponentsIndex name to Components
 - Changed FormioForm name to Webform
 - Changed FormioWizard name to Wizard
 - Changed FormioPDF name to PDF
 - Moved Formio.fieldData to FormioUtils.fieldData
 - Input elements within a DataGrid now refer to the "rowIndex" instead of the column index within the "name" attributes.
 - Chnaged the wrapper classes for Radio and Select Boxes components to be "form-group" instead of "input-group" to make it compatible with both Bootstrap 4 and Bootstrap 3.
 - Renamed GMap component to Location component
 - Changed all exports on Components to be default exports. ```import TextFieldComponent from 'formiojs/components/textfield/TextField';```
 - Deprected ability to "attach" Formio to existing form using Formio.form method.
 - Changed the name and ids of Radio buttons within DataGrids to reflect their position in the grid.
 - Modified all JavaScript execution and template interpolation to make it more consistent.
   - "component" now always refers to the JSON of the component (not the component instance)
   - "instance" now refers to the component instance. Use at your own risk of SDK changes within each component!
   - "row" always points to the "data" context object for that instance (typically row in DataGrid)
   - "data" always refers to the global data of the submission.

## [Unreleased]
### Fixed
 - Data Grid excess re-rendering rows on setValue

## 3.0.0
### Fixed
 - Issue where components in table component would not render conditions correctly.
 - Issue with the selection of a radio component.
 - Multiple Select: Fixed selected items being rendered outside of the input

### Changed
 - Upgraded fetch-mock@6.5.2, gulp-watch@5.0.1, karma@2.0.5, sinon@6.1.4, webpack@4.16.3, i18next@11.5.0, eslint@5.2.0, gulp-rename@1.4.0

## 3.0.0-rc.26
### Fixed
 - Issue with the PDF builder where it would constantly update pdf components when it didn't need to.

## 3.0.0-rc.25
### Fixed
 - Issue where the indexes on EditGrid would get messed up and could add bogus entries.

### Added
 - The lazy load setting for Select components.

## 3.0.0-rc.24
### Fixed
 - Issues with the edit forms not overriding correctly causing inconsistencies with the forms for components.
 - Error for Data Grid with invisible columns (Hidden components, conditionally hidden fields etc.)
 - Issue with EditGrid where the form would invalidate when you are filling out a new row.
 - Search placeholders on the Select dropdown.

### Added
 - CSS classes for array components buttons
 - dataGridLabel configuration when a component is within a DataGrid element.

## 3.0.0-rc.23
### Fixed
 - PDF builder to work much better with the drop zone handling for remote pdf forms.
 - Fixed Data Grid components labels being rewritten to false
 - Hidden Component value being equal to '[object Object]'
 - DataGrid in the builder to allow for editing of the data grid.

### Added
 - Allow for editForm overrides when embedding the form builder.
 - A way to include a "namespace" for the tokens added to your browser so this library can handle multiple projects at once.

## 3.0.0-rc.22
### Added
 - Word and character counts along with validation to all text components.

### Changed
 - Upgraded i18next@11.3.6, babel-eslint@8.2.6, eslint@5.1.0, webpack@4.16.1

### Fixed
 - Utils `getComponent()` function.
 - Data Grid displaying column for Hidden field
 - Fixed the 12hr time configuration for DateTime component.

## 3.0.0-rc.21
### Fixed
 - Issue with builder where editing a component would not work inside nested component.
 - Fixed data grid to not show columns consisting of hidden components.
 - Decimal separators for languages that do not use numerics.

### Added
 - Configure dragula to check if a component can be dragged using the 'no-drag' class

## 3.0.0-rc.20
### Fixed
 - Problem where conditionally hidden select fields would not resolve their loaded promise.

## 3.0.0-rc.19
### Changed
 - Made each build entry derive from the same formio.form entry.

### Added
 - The ability to have access to the Promise library from external mechanisms.

## 3.0.0-rc.18
### Added
 - A way to force components visible or hidden in a hierarchial manner.
 - A way to get access to Formio.Utils from the global Formio object.

## 3.0.0-rc.17
### Added
 - A way to get access to the Formio.Components from within a global script.

## 3.0.0-rc.16
### Fixed
 - Issues with all Nested components getting the "tree" parameter which messed up validators for non data components.

### Changed
 - Upgrade flatpickr@4.5.1, i18next@11.3.5, babel-loader@7.1.5, eslint@5.0.1, fetch-mock@6.5.0, sinon@6.1.3, webpack@4.15.1, gulp-eslint@5.0.0

## 3.0.0-rc.15
### Added
 - Possibility to override i18n settings.
 - `focus` and `blur` events.
 - Added uploadOnly to file component

### Fixed
  - Nested forms validation.

## 3.0.0-rc.14
### Fixed
 - Bad build from previous release.

## 3.0.0-rc.13
### Added
 - Ability to not show any buttons in rendered form.
 - Better feedback on the submit buttons when form is submitting and errors occur.

### Fixed
 - Wrong data being passed to EditGrid and DataGrid for some evals.

## 3.0.0-rc.12
### Fixed
 - Problem with the PDF Builder where you would not see the builder elemements.
 - Fix default value on checkboxes.
 - Fix multiple required file fields not requiring uploading a file.

### Added
 - Make rowIndex available on editgrids and datagrids.
 - Add custom class name to table component.
 - Add the ability for events to trigger field logic.
 - Add option to trigger validations when button is pressed.

### Changed
 - Upgrade i18next@11.3.3

## 3.0.0-rc.11
### Fixed
 - Some issues with the Formio constructor to determine the project, form, and submission paths for certain urls.
 - Problem with the form builder where it would not add elements to the correct parents, but rather the root form.

### Changed
 - Moved the dynamic library loader into the Formio lib so that it is available to other libraries without renderer.

### Added
 - Okta SSO integration.

## 3.0.0-rc.10
### Added
 - Fontawesome for button icons.

### Fixed
 - Multiple require file field not requiring files.
 - File component for base64 download event.
 - Cleanup of editgrid code.

## 3.0.0-rc.9
### Changed
 - Default value for calculated logic.

### Fixed
 - Issues with the event system where some events would get canceled by other components.
 - Required validation for Survey component.
 - Fixed an issue where the file service is not defined when removing images from file component.

### Added
 - Allow url uploads to respond with their own url.
 - 'Hide Input Labels' property for Day component.

## 3.0.0-rc.8
### Fixed
 - Problem with the Select component where it would remove selected items while searching.
 - Issues with the "ready" call after setSubmission would call to early when Select items have not been loaded.
 - Problem with the DateTime component onFocus event opening the calendar on readOnly forms.
 - Problem where the DateTime calendar would still be open when the component is disabled.

### Added
 - Option to allow the HTML and Content components to refresh when a value changes in the data.

### Changed
 - Added deprecation notice to "whenReady" method and replace it with dataReady getter property.

## 3.0.0-rc.7
### Added
 - A builder css build without font-awesome to fix issues with framework library implementations.

## 3.0.0-rc.6
### Fixed
 - Moved all of the function and interplation context objects to use the same method so all available items within are consistent.
 - Problem where the errors of components inside of nested components would not reset the error messages.
 - Problem where Radios within datagrids were getting same name attributes and click events would select the wrong row.

## 3.0.0-rc.5
### Fixed
 - Fixed bad deployment.

## 3.0.0-rc.4
### Fixed
 - i18n in File component.
 - `viewAsHtml` for nested forms.
 - Fix the Day component required validation to work with independent inputs.
 - Fixed the checkbox DOM states to mirror the actual state of the checkbox.
 - Ensure we don't call setInputStyle without an input.
 - Fixed the datetime default date and fixed console warning from moment.

### Changed
 - Only trigger error events on nextPage and submissionError events.
 - Set the value to the checkbox component value when using component name, like in Radio configuration.
 - Moving the fieldData method to FormioUtils.
 - Allow for fully loaded nested forms to render without hitting the server.

### Added
 - Adding the component instance to the change events.
 - Adding the pdf source information to the form object.

## 3.0.0-rc.3
 - Bad release

## 3.0.0-rc.2
### Fixed
 - Issue with Bootstrap.js messing up the form builder accordion.

## 3.0.0-alpha.20
### Added
 - Possibility to Disable Adding / Removing rows for Data Grid
 - Adding numRows and numCols to table builder.

### Fixed
 - Hide the label component for table editing.
 - Fixing the schema creation to not turn arrays into objects.
 - Fixing how datagrid appends names to inputs.
 - Ensure that the error check is fired when changed and submission. Also reset errors when conditionally hidden.
 - Ensure new components added with builder get unique api keys.
 - Fixed issues with number component where it would not submit.
 - Fixed an issue where the number component would not reset its value.

## 3.0.0-alpha.19
### Fixed
 - File data for url file uploads getting lost if it doesn't contain a .date property.

## 3.0.0-alpha.18
### Fixed
 - Issue with multiple settings on Select component not allowing a submission.
 - Problem with the Day component setting disabled where it would cause javascript error.
 - Styling problems with Bootstrap 4 and radio and checkbox controls.
 - Default value issues with the Day component.
 - Problems with non-set values getting set within the submission data.

## 3.0.0-alpha.17
### Fixed
 - Issues with the table builder where it would remove elements when building existing forms.
 - Select component to not have static search enabled for URL based selects with searchField set.
 - Fix possible issue with eachComponent that tries to iterate over a non array.
 - Fix the PDF renderer so that it will submit the form correctly.
 - Fixed issue with the errors disappearing after they show up.
 - Fixed issue with Checkbox configured as radio where original boolean would not get set with submission.
 - Fixed the input disabled class to be dynamic based on the disabled state of the component.
 - Fixed issue where isValid method would return false on hidden required fields.
 - Fixed issue where the x button on multiple select dropdowns was showing in read only mode.

### Changed
 - Make sure to default persistence to true unless otherwise stated.

### Added
 - A way to turn of the static search for select fields in the form builder.

## 3.0.0-alpha.16
### Fixed
 - Issues with the columns builder not including its components.
 - Problems with the decimal place identifier not working for number components.
 - Problems with the file upload not able to get the "formio" instance from the root object.

### Changed
 - Made the default table configuration a static property for ease of maintenance.

## 3.0.0-alpha.15
### Fixed
 - Problem with the Columns builder where it was not adding columns.

## 3.0.0-alpha.14
### Added
 - Possibility to unselect value for Select component.
 - Possibility to show hidden fields using options

### Fixed
 - How TextArea is rendered when it is configured as wysiwyg and is being viewed as readOnly
 - Problem where malformed functions in "custom" parameters could crash renderer.
 - Issues with the Checkbox component configured as a Radio not setting values correctly.
 - Require Decimal behavior for Number and Currency components
 - Hide Label functionality for Panel component
 - Tooltip being hidden for Panels when label is hidden

### Changed
 - Upgraded i18next@11.3.2 flatpickr@4.5.0

## 3.0.0-alpha.6
### Changed
 - The library structure
 - Now using Webpack for the builds.

### Added
 - Multiple masks for text field and phone number components

## 3.0.0-alpha.5
### Fixed
 - Issues with the simple conditional logic in form builder.

## 3.0.0-alpha.4
### Added
 - Better documentation around the javascript execution code.
### Fixed
 - Issues with text area not working when set to required.
 - Problems where two text with same key not working in form builder.
 - `moment` library inside calculated value for DateTime component.

## 3.0.0-alpha.1
### Added
 - Form Builder
 - Tags component (advanced)
 - Tabs component (layout)
 - Collapsible panels
 - A way to remove event listener using the "off" method.
 - "hasClass" method to check for a class.
 - "hasValue" method to check for a value within a component.
 - Version number and license link in all builds.

### Changed
 - How logic executions work by moving them into a single location within FormioUtils called "execute".
 - Made a single way to create modals for form builder and resource adding.
 - Now include Formio utils in the basic "formio" library under Formio.Utils

### Removed
 - Lib folder since this will be included in the package build.
 - Dist folder since this will be included in the package build.

### Fixed
 - Make sure to pass the full root data object within checkValidity.
 - Folder name for EditGrid component.

## 2.32.1
### Fixed
 - Issue with the OAuth button where it would launch the modal at the wrong times.
 - Problems where clearOnHide would trigger on readOnly forms.

## 2.32.0
### Added
 - Ability to save a submission in a state (Save in state on button)
 - Ability to skip frontend validation if in draft state
 - Delete action to button component
 - Message on file component when validation fails

### Fixed
 - Nested form data handling.
 - Default values on nested forms.
 - DateTime component resetting values was not working.
 - Validation styling inside datagrid
 - Destroy method on wizard component not removing header and footer
 - Problem where number component would crash if decimalLimit was less than 2.

### Changed
 - Upgrade i18next to 11.2.3

## 2.31.4
### Fixed
 - Disappering label for DataGrid.
 - Validation for DataGrid.
 - Validation for EditGrid.
 - Destroy method should clear form element
 - Stop talking about FFiles.

### Added
 - Add basic support for submission states.
 - Docs about Seamless.js integration.
 - Explain why files have been rejected when validation fails.

## 2.31.3
 - Bad Release. Do not use!

## 2.31.2
### Fixed
 - Problems with datagrid not rending properly and getting out of sync.
 - Issues with the minLength and maxLength on data grid.
 - Performance issues with datagrid to not re-render unless it needs to.
 - Problem with multiple value setting not resetting values when removing rows.
 - Flickering UI when adding and removing rows from a data grid.

## 2.31.1
### Changed
 - Updated build with latest dependencies.

## 2.31.0
### Fixed
 - Display of Dates within edit grids.

### Changed
 - Server errors now return a rejected promise instead of throwing an error.

### Added
 - Nested form support for forms of different types.
 - Data variable in editgrid templates
 - Collapsible fieldsets
 - Autofocus feature.
 - `getView(component, data)` option for EditGrid body template.

### Fixed
 - Interpolation for EditGrid.

### Fixed
 - Select HTML5 component with Custom data source.

## 2.30.2
### Fixed
 - Problem where values would not get reset before getting deleted with clear on hide.
 - Issue where change events would fire continuously because of eroneous hasChanged checks.

## 2.30.1
### Added
 - `moment` library in calculated value and advanced conditional.
 - Add ability to pass options to currentUser function.

### Changed
 - Removed the duck-punch from choices library for strict equality since they pulled in our pull request.

### Fixed
 - Empty string in email validator.
 - Min-max for DataGrid component.

## 2.30.0
### Fixed
 - Required validator for Checkbox component.
 - Radio and SelectBoxes components for the case with multiple nested forms.
 - Number and Currency components default value.
 - Input mask problems where a single instance was used to manage multiple inputs.
 - Issues with onChange events not firing for Select components.
 - Streamlined the language inititalization.

### Added
 - Better data handling using getters and setters.

### Changed
 - Deprecating "getRawValue" with reverse compatibility in favor of component.dataValue.
 - Made currency component to have a delimiter unless specified otherwise.

## 2.29.13
### Fixed
 - Problem with some crashes within the file component.
 - Make sure the Submit button was not disabled even if form was readonly
 - Problem with the DataGrid component default values copying from row to row.

### Added
 - The ability to prevent a component from being disabled with a "alwaysEnabled" property.

## 2.29.12
### Fixed
 - Custom events not firing for button custom events.
 - Issue with conditoinals not checking on form components before loading subforms.

## 2.29.11
### Changed
 - Upgraded browserify@16.1.1 eslint@4.18.2 fetch-mock@6.0.1 mocha@5.0.4 watchify@3.11.0 gulp-strip-debug@3.0.0 marked@0.3.17
 - Added exports that are reverse compatible with ES5.

### Fixed
 - Display for resource fields within submission grid.

## 2.29.10
### Fixed
 - Issues with getView so that it does not throw errors.
 - Min and Max settings on DataGrid to stop showing Add Another button.

## 2.29.9
### Fixed
 - Issues with IE not translating Date's properly.

## 2.29.8
### Fixed
 - Include polyfill for bind to fix PDF generation.

### Changed
 - Upgraded i18next to 10.5.0

## 2.29.7
### Fixed
 - Fix validations automatically triggering if you have only a container on a form at the root level.

## 2.29.6
### Fixed
 - Fix validation and nested form issues with wizard.

## 2.29.5
### Fixed
 - Ensure that the form components do not load if conditions on the component return false.

## 2.29.4
### Added
 - More input hooks to certain components.

### Fixed
 - Issue where file component values would reset.

### Changed
 - The select component will now enable search by default and can be turned off with "searchEnabled" flag on component.

## 2.29.3
### Fixed
 - Issue with the providers not getting registered correctly.

## 2.29.2
### Changed
 - Upgraded i18next to 10.4.1

### Fixed
 - Problem where DataGrid could add duplicate columns.

### Added
 - Add ability to have oauth initiated logins.

## 2.29.1
### Added
 - 'Delimiter' property to Number component.
 - Error message below submit button.
 - WYSIWYG spellcheck option for the Quill editor.

### Fixed
 - Issues with clearOnHide
 - Fixed radio button wrapping issue
 - Problems with the wysiwyg editor clearing values within a datagrid.
 - Asterisks for Checkbox component with 'inputsOnly' option.
 - The Formio.cache to return new promises instead of using old ones.

### Changed
 - Cleanup and performance improvements on how conditions are checked and evaluated.
 - How the loader icon is added to the renderer by adding an additional DOM element above the form components.
 - Upgrade flatpickr to version 4.3.2
 - Improved viewAsHtml and asString features.

## 2.29.0
### Added
 - New Field Logic feature.
 - Ability for buttons to be configured with a URL that will send the submission to that url when pressed.

### Changed
 - Upgraded all dependencies.
 - Reverted choices.js to use npm version and duck-punch the deep equality checks.

### Fixed
 - Issue with Required WYSIWYG TextArea always triggering validation error on load.
 - Problem where backspacing the wysiwyg editor was not working.
 - Problem where tabbing into a wysiwyg editor would select buttons on the wysiwyg.
 - Problem with the Form component where it would load the form when a default submission is provided.
 - Performance issues with both EditGrid and DataGrid.
 - Issue with false conditionals and null values.
 - Issue with the "render" event not firing when form is rendered.
 - Problems with the viewAsHtml flag not rendering the submission.

## 2.28.6
### Added
 - Autofocus capability.
 - Ability to provide spellcheck parameter to input.

### Fixed
 - Some issues with subforms when performing calcuated values
 - Problems with subforms performing the load when they are not conditionally available.

## 2.28.5
### Fixed
 - Issue with input mask crashing when no input mask is on the field.

## 2.28.4
### Added
 - Mask validator for Phone Number.

### Fixed
 - Default value for component with input mask.

## 2.28.3
### Changed
 - The conditional logic where a parent that is conditionally invisible is overridden by a child conditionally visible.
   This logic is different from the Angular 1 renderer, so we made it consistent where a conditionally visible child will not
   override a conditionally hidden parent. However, this behavior can be changed by providing the "conditional.overrideParent" flag
   on the child component.

## 2.28.2
### Fixed
 - Issues with the sub-form component not loading the proper source for remote servers.
 - Issues with the sub-form component not passing along sub data to conditional checks properly.

## 2.28.1
### Fixed
 - Text mask dependencies

## 2.28.0
### Added
 - Support for Bootstrap 4
 - EditGrid Component.
 - Stripe integration within Contrib.

### Fixed
 - Small problem with read-only file uplaods where it would allow you to remove files.

## 2.27.6
### Fixed
 - Issue where the ready promise was not getting fired if a submission is not provided.

## 2.27.5
### Fixed
 - The package.json for the choices.js library to not use a git url.

## 2.27.4
### Added
 - The ability for the search to be an array of values.

## 2.27.3
### Fixed
 - Issue with the checkCalculated method not working for datagrids.

## 2.27.2
### Added
 - Support for OAuth buttons in the renderer.
 - Ability to add the "Add Another" button on datagrid to either above or below the grid.

### Fixed
 - Problem where a padding-right is applied to all has-feedback inputs even though an icon is not used.

## 2.27.1
### Fixed
 - Problem with default values on wizards.
 - Issue where row is not passed to calculated values.
 - Select Resource component searching.

### Added
 - Ability to auto load the initial values for lazyLoad select with search enabled.
 - CSS class ('radio-selected') for selected option of Radio component

## 2.27.0
### Fixed
 - Issue where read-only forms would still try to submit.
 - Problem with read-only wizards triggering beforeSubmit handlers.
 - Fix issue where submissions made before revisions are made will sometimes cause the form to not load.

### Changed
 - Upgrade all dependencies

## 2.26.2
### Fixed
 - Problem where a component has input should also return true if it has inputs.

## 2.26.1
### Fixed
 - Problems where data keys are added even if component is not set with input.
 - Failing tests.
 - Datagrid data merging.

### Changed
 - Upgraded choices.js to 3.0.3 which includes performance fix.
 - Removed performance hack in Select since 3.0.3 of choices resolves the problem.

## 2.26.0
### Added
 - New contributed module system with Stripe integration.
 - A way to pass the formio instance object to the currentUser and accessInfo methods.

## 2.25.8
### Added
 - Support for JSONLogic dates.
 - Added 'searchEnabled' option and defaulted it to false, user can enable it with component property
 - Updated default value for 'removeItemButton' option to multi-select OR false, and if needed user can enable it with the component property
 - Date formatting based on the locale configuration
 - viewAsHTML feature.
 - Confirmation dialog before a form/wizard is canceled.

## 2.25.7
### Fixed
 - Problem with the Select dropdown from re-rendering after it has been destroyed.
 - Issue with the default select for html5 widgets.

### Changed
 - Upgrade moment to 2.20.1

## 2.25.6
### Added
 - Ability to dynamically alter text based on input data.
 - Try/catch around the jsLogic for checkconditionals.
 - LazyLoading for select dropdowns.

### Fixed
 - Caching issue with getTempToken method.
 - Problem with the "in" operator for JSONLogic crashing with null inputs.

## 2.25.5
### Fixed
 - getDownloadUrl to work with remote environments.

## 2.25.4
### Fixed
 - Problems where conditionally hidden panels/wells were not making their children not required.
 - Issues with setting default values on datagrids.

### Added
 - Ability to provide an input mask where it will force lowercase alphabetical.

## 2.25.3
### Fixed
 - An issue where data values within a datagrid get messed up when rows are removed.

## 2.25.2
### Fixed
 - A problem with Select dropdowns where the placeholder was getting included as the select value.

## 2.25.1
### Fixed
 - Problem with the FormComponent crashing during a set language within the constructor.

## 2.25.0
### Added
 - The ability to render Select component as plain select dropdown using widget: 'html5' setting.
 - Performance improvements to language selection

### Changed
 - Moved all translation capabilities into FormioForm for performance reasons.

### Fixed
 - Issues with Lodash operators for JSONLogic.

## 2.24.6
### Changed
 - Upgraded EventEmitter2 to version 5.0.0
 - Upgraded flatpickr to 4.1.4

### Fixed
 - Major performance problems with the Select component with large datasets.

## 2.24.5
### Fixed
 - Problem where pressing enter in a textarea would submit the form.

## 2.24.4
### Fixed
 - Problem where change event would not get fired when a row is removed from datagrid.

### Added
 - Options to control the navigation and breadcrumb in wizards.

## 2.24.3
### Added
 - Ability to provide HTML in the description of a form element.

### Fixed
 - Double submit issue with wizards.

## 2.24.2
### Fixed
 - Issue loading form after submission when revisions not enabled.

## 2.24.1
### Fixed
 - Date min and max settings.

## 2.24.0
### Fixed
 - File component inside Datagrid component.
 - Components with label position inside Datagrid component.

### Added
 - Interpolation to the select headers when requests are made.
 - Option to make the wizard header buttons not clickable.
 - Translations to the select dropdown elements.
 - Form version handling

## 2.23.2
### Fixed
 - Path parameter for cookie fallback functions.
 - Custom calculated values.

## 2.23.1
### Added
 - Method and POST body to select dropdowns.
 - Lodash operator to JsonLogic.

### Fixed
 - Added custom classes to column components.
 - Checkbox required validation with 'name' options set.

## 2.23.0
### Added
 - Possibility to specify label position for component and for options for Checkboxes and Radio components.

## 2.22.2
### Added
 - The ability to pass an array of errors to the error handler to show more than one.
 - The ability to make independent components invalid.

## 2.22.1
### Fixed
 - A promise issue with executeSubmit method in FormioForm

### Added
 - Custom data source to Select component.

## 2.22.0
### Fixed
 - Fixed an issue where the token-cookie fallback was not returning the token
 - Forms not recusing properly in eachComponent function.

### Added
 - Possibility to add shortcuts.
 - A new hook system that allows to easily create hooks within the renderer.
 - 'beforeSubmit' hook to configuration.
 - 'input' hook to call when new inputs are added.
 - Display custom validation error message.
 - Ability to inject form data into the error messages.

## 2.21.3
### Added
 - A more robust way to determine if the form is completely loaded and ready.

## 2.21.2
### Fixed
 - Fixed the pdf generation by moving bind polyfill before dependant libraries.

## 2.21.1
### Added
 - A way for the components to hide their labels and have them set using the hideLabel option.
 - A way to pass in headers to a request in JSON format.

## 2.21.0
### Changed
 - Upgraded all dependencies

## 2.20.5
### Fixed
 - Problem with Select compoenents not updating values within a wizard.
 - Issue with setting default object values of select components.
 - Problem with duplicate entries showing up in select components when default objects are used.
 - Issue where clearOnHide was too aggressive in when it should clear out data.

### Changed
 - Display original file name instead of unique name on File component.

## 2.20.4
### Fixed
 - Problem with Resource dropdowns not working due to the unset options variable.

## 2.20.3
### Fixed
 - Problem with cookie fallbacks on file uploads not working.
 - Editing nested forms mapped to another resource with save as another resource fails.

### Changed
 - Now allow the URL of Select dropdowns to simply return strings of JSON and it will parse at runtime.
 - Upgrade Flatpickr to 4.0.5

## 2.20.2
### Fixed
 - Issues with using for in statements with arrays pulling in keys we don't want.
 - The data view of a Signature to show the image of the signature for easy scaling.

### Changed
 - The Select dropdown api requests to use Formio.makeRequest so that plugins could be used.
 - Upgrade Quill.js to 1.3.3

## 2.20.1
### Changed
 - Upgraded Flatpickr to 4.0.4 to fix crash in IE.

### Added
 - Global option to not show the datepickr for date inputs.

### Fixed
 - Issue where a null flatpickr instance would crash renderer.

## 2.20.0
### Added
 - Much better i18n support for Number and Currency components.

### Fixed
 - Added file input to DOM as a hidden item to fix issue with IE
 - Select component to respect tab index
 - Resize issues with Signature component so they scale according to devicePixelRatio.

### Changed
 - Force dropdowns to open only downwards
 - Upgrade moment to 2.19.1 since they fixed React bug (https://github.com/moment/moment/issues/4216)

## 2.19.3
### Fixed
 - Downgraded moment to 2.18.x to fix an import issue with Webpack.
 - Changed the SignaturePad module to directly include the library to fix React app issues.

## 2.19.2
### Fixed
 - Form component to allow recursive loading and setting a submission value.

### Changed
 - Upgraded moment to 2.19.0

## 2.19.1
### Fixed
 - Problem with multi-form workflows showing the submission not showing all data.

### Changed
 - Changed debounce to 100ms to make forms seem faster.

### Added
 - Redirect capabilities within the embed code.

## 2.19.0
### Fixed
 - Performance issues with large forms with conditionals.
 - Issue with select list not saving values accross pages.
 - Fixed issue with prepend not working if no firstChild is provided.
 - Loader from not showing up.
 - Issue with the form component not validating correctly.
 - Issue where the DateTime component calendar would not show up.
 - Better fallback for cookie support if localStorage is disabled or not present.
 - Add Editgrid and custom components to recursive tree.
 - Issue where conditionally visible components should also force parents visible.
 - Allow email components to be valid if pristine and empty.
 - Issue where clearOnHide flag was not working.
 - Issue where tooltips were not showing up on DataGrids
 - Issue where a form would invalidate after a successful submit.
 - Problem with setting a radio button with boolean values.

### Added
 - Support for HTML within tooltips.
 - Added a way to render the full wizard with conditional pages.
 - Ability to provide custom error messages per component using an errors property on each component.

### Changed
 - Convert line feeds into <br/> statements for tooltips.
 - Wizard to allow for hidden fields to be passed through all pages.

## 2.18.0
### Fixed
 - Fixed the validity checks and button disabled states.
 - Fixed the error message on regular expression settings.
 - Issue with the default values not working on Select dropdowns.
 - Fixed the input mask to show only number pads on all numeric inputs.
 - Performance when using conditional logic. checkConditionals called too many times on submission set.

### Added
 - Ability to handle dynamic min and max dates.

## 2.17.6
### Fixed
 - Fixed the search input to work with select fields.
 - Fixed the Radio components to allow for boolean and numeric values.
 - Fixed the disabled flag to not allow add another options, and fixed button on disable.
 - Fixed an issue with a crash that was causing selectboxes to not render within a data grid.
 - Fixed issue where the errors would not show up on Radio elements.
 - Fixed the DateTime calendar to only open the calendar if it has not already been closed.

## 2.17.5
### Added
 - minDate and maxDate for DateTime fields.
 - Custom headers for the requests of a select dropdown.

### Fixed
 - The calendar to hide and show when the icon is clicked.
 - Issues where placeholders would not show up in the DateTime component.
 - Default dates for DateTime component.

## 2.17.4
### Fixed
 - Issue where calculated values were not getting triggered on form component.
 - Issue where the forms would not load within the form component.

## 2.17.3
### Added
 - Tooltip feature onto the fields within the rendered form.

### Fixed
 - Issue with the form component not loading subforms for view pages.
 - Issue where HTML components were not interpolating the text.
 - Use handler.type instead of undefined handler.event property

### Changed
 - The default sort of the Choices library to not sort by default.

## 2.17.2
### Fixed
 - Issues with translations and certain strings that contains special characters.
 - Issues with the Select drop down pulling the wrong url to send the request off to.

### Added
 - Mask input fields when set.

## 2.17.1
### Fixed
 - Don't try to access properties of null in getValue.

## 2.17.0
### Added
 - Set lang attribute on all input elements based on current language. This helps with number localization.
 - Added better placeholder support for select dropdowns.

## 2.16.1
### Fixed
 - Colon in field name.

## 2.16.0
### Added
 - Cookie fallback for storing tokens and user values.

### Fixed
 - Default values overriding values when new form is set.

## 2.15.2
### Added
 - Ability to respond to ajax requests in a plugin.

## 2.15.1
### Added
 - Ability to introduce custom file service classes.

### Fixed
 - The PDF download url logic to return the correct download url.

## 2.15.0
### Added
 - Better multi-language support.
 - Min and Max validation checks for number fields.

## 2.14.1
### Fixed
 - Some minor crashes with the PDF renderings.

## 2.14.0
### Added
 - PDF support

### Changed
 - Upgraded dependencies

## 2.13.6
### Added
 - Add error labels.
 - Exposed ```util``` for Calculated Value.
 - ```parseFloat``` extension on FormioUtils.
 - ```formatAsCurrency``` function on FormioUtils.
 - A way for the setValue to take an object of flags instead of function params.

### Fixed
 - An issue where an infinite loop would trigger for calculatedValue's.

## 2.13.4
### Added
 - Resource modal to add new resources inline within form.
 - Custom scripts to be executed on button click.

## 2.13.2
### Added
 - Allow plugins to modify request options before they are sent.

## 2.13.1
### Added
 - A way to determine if a user is able to submit a form before they do.
 - A delete api call when a file is deleted.
 - A way to upload base64 file uploads.

### Changed
 - Refactored the http requests to have less Promises and more streamlined.
 - Wait for the form to load before loading the submission.

### Fixed
 - Fixed some issues with multi-select field validation.

## 2.13.0
### Fixed
 - Issue where Selectboxes was not storing the correct data structure.
 - The disabled states on all components.
 - Issue where Formio.createForm was not establishing the formio object on src load.
 - Problem where conditionally hidden components were still validating when they shouldn't.
 - Issues with auto-population for conditionally hidden components.
 - Auto population for the Address component.

### Added
 - Component error highlights when an error occurs during invalidation.
 - Custom styles capability.

### Changed
 - All instances of jsonLogic to use the FormioUtils.jsonLogic so that it can be extended.

## 2.12.3
### Added
 - Ability to pass a query to getComponent.

## 2.12.2
### Changed
 - Allow the FormioUtils to be globally accessible.

## 2.12.1
### Changed
 - Upgrade Choices to 2.8.7
 - Upgrade Flatpickr to 3.0.6
 - Upgrade json-logic-js to 1.1.3

### Added
 - A new findComponents method for locating components based on search queries.

## 2.12.0
### Added
 - A register component method to register custom components.

### Changed
 - Remove templating from ce function.
 - Replace Handlebars templating with lodash.

### Fixed
 - An issue with the select boxes component that showed required astrix on all options.

## 2.11.8
### Fixed
 - Issue where choices.js changed internal api that we rely on.

## 2.11.7
### Added
 - Description support for fields.
 - WYSIWYG editor for the text area component to use Quill.js

## 2.11.6
### Fixed
 - Another instance where infinite JSON structures could occur with eachComponent.

## 2.11.5
### Fixed
 - Issue where the parent property could create infinite JSON structures.

## 2.11.4
### Changed
 - Do not introduce the parent property on eachComponent unless a root is provided.

## 2.11.3
### Added
 - The ability for eachComponents to reference its parent component.

## 2.11.2
### Fixed
 - An issue where if you set the url of the form, it should not submit to API.

## 2.11.1
### Fixed
 - Issue with including handlebars in other libraries with webpack.

## 2.11.0
### Added
 - Now using Handlebars as the template interpolator.

### Fixed
 - Issue where the eval code for calculatedValues and defaultValues was causing an error.
 - Removed deprecated getAppUrl within the Resource compoennt.

### Changed
 - Changed the this.src setter to use the this.url for reduced code duplication.

## 2.10.1
### Fixed
 - Issue where form would crash if choices was not present.

## 2.10.0

### Added
 - Custom class capabilities to all components.
 - defaultDate to the Date/Time component.
 - File component

## 2.9.10
### Changed
 - Upgraded jsonLogic library to 1.1.2.
 - Removed the unnecessary embed method in formio.form.js. Use formio.full.js to bring it back in.

### Fixed
 - Issue with the multi-page forms where the conditions would not apply properly.

### Added
 - Time Component

## 2.9.9
### Added
 - Support for conditional wizards.

## 2.9.8
### Added
 - A way to print out the text of a component with a value.

### Changed
 - Added a way to create a componenent but not build it.

## 2.9.7
### Fixed
 - An issue where Select components were not selecting the default values properly.

## 2.9.6
### Added
 - A formLoad event to fire when the form is done loading.

## 2.9.5
### Fixed
 - Issue where if you try to re-enable disabled fields, it wasn't working.
 - Added a getter for the visible state of fields.

## 2.9.4
### Changed
 - Upgraded all dependencies to latest versions.

## 2.9.3
### Fixed
 - Ensure the full.js is in the npm build.

## 2.9.2
### Fixed
 - Other reverse compatible issues.
 - The embed code to also work with Wizards.

## 2.9.1
### Fixed
 - The import process so that it is reverse compatible.

### Added
 - Formio.full CSS.

## 2.9.0
### Changed
 - Removed the formio-factory file in exchange of formio.full.min.js.
 - Attached createForm method to main Formio object.

## 2.8.8
### Added a formio factory to the dist folder.

## 2.8.5
### Fixed
 - Issue where the custom events were not firing properly on buttons.

### Added
 - Custom classes to the button component.

## 2.8.4
### Fixed
 - Issue where submission binding with columns in datagrids was not working.
 - Fixed issue where adding another item to datagrid would clear out rows.
 - Problem where datagrid rows would add going between wizard pages.

### Added
 - CSS classes to wizard navigation buttons.

## 2.8.3
### Fixed
 - Bad binding with radio buttons in datagrids.
 - Issue where custom classes would not get applied to checkboxes.
 - Default values applied to datagrids and containers.
 - Issue where the loader would continue to be present during an error on load.

### Added
 - Custom event triggers for custom event buttons.

## 2.8.2
### Fixed
 - Submit button handler.

## 2.8.1
### Fixed
 - Fixed the json form select dropdown.
 - Fixed issues with button events and form submissions.

## 2.8.0
### Added
 - Support for multi-page form workflows.

### Fixed
 - Data grid select lists
 - Checkbox inputs to not use class when no label is present.

## 2.7.3
### Changed
 - All disabled flags to be consistent.

### Fixed
 - Issue where submit button would not disable.

## 2.7.2
### Fixed
 - Some cases where errors would occur during rendering.

## 2.7.1
### Fixed
 - An issue where Radio buttons could cause javascript error.

## 2.7.0
### Added
 - JSONLogic to perform all validations, conditionals, and calculations.

### Fixed
 - Fixed many issues with validations, conditionals, and calculations.
 - Fixed the disabled flag to disable on start.
 - Fixed default values to work.

## 2.6.0
### Changed
  - Upgraded the fetch library to resolve some strange header response caching issues.

## 2.5.0
### Added
 - JavaScript SDK logic to easily get the temporary tokens using the new temp token api.
 - Adding conditional next pages to the Wizard functionality.

## 2.4.2

### Changed
 - Moved the logout token and cache clearing to before the call is made to the server.

### Fixed
 - Bizarre issue that seems to be a bug in browser "fetch" library where it would introduce a response
   JWT token when a request was made without one. It was verified that the server was not sending
   the token in the response, so it is concluded that for some reason fetch was introducing it (cache maybe?).
   Regardless, we fixed it so that it will detect when a token was introduced and throw it out.

## 2.4.1
### Changed
 - Renamed setAppUrl to setProjectUrl
 - Renamed getAppUrl to getProjectUrl

### Deprecated
 - setAppUrl is now deprecated
 - getAppUrl is now deprecated
