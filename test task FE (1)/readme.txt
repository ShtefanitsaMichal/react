As a result of this task there should Redux based web application (http://redux.js.org/docs/introduction/). 

Task Description:
Please add the TWO dropdowns to the index page which will show the list of countries. Data structure for list of countries is next:
{
    selectedCountryId: '2',
    countries: [{
            id: '1',
            name: 'Ukraine'
        },
        {
            id: '2',
            name: 'USA'
        },
        {
            id: '3',
            name: 'England'
        },
        {
            id: '4',
            name: 'Spain'
        },
        {
            id: '5',
            name: 'Poland'
        }]
}

The project should include following parts: 
index page:
	index.html - html page which contains our SPA app, 
	index.scss - it should contain styles for Index page and include scss files of other components used on Index page.
	entry.js - entry point of our Redux application. Entry point should contain usage of the container.
	container.js - container which contains the usage of the DropDown react component.
	actions.js - actions of the Index page. There should be init action. 
	reducers.js - index page storage. It should store data which will be displayed in DropDown.

dropdown:
	dropdown.jsx - react component which represents dropdown and its logic. This component should render the list of DropDownItem components.
	dropdownItem.jsx - react component which represents one item of the dropdown. This component should be used as child of the DropDown react component.
	dropdown.scss - styles of the dropdown component.

The js files should be built with webpack.
The scss should be compiled into css with the gulp.
As output there should be next files: bundle.js and styles.css.
 


Acceptance criterias:
- dropdown should look the same as in dropdown.psd file
- DropDown react component should have next properties:
     - onSelectedValueChanged - this callback should be called when the value in dropdown was changed,
     - title
- DropDownItem react component should have next properties
     - text,
     - value,
     - isSelected

- DropDownItem should be passed as children to DropDown:
	<DropDown> 
		<DropDownItem />
		<DropDownItem />
		...
	</DropDown>
- dropdown should select item which has 'isSelected' property of the DropDownItem set to 'true',
- selected item should be highlighted (#1 in the 'dropdown-screen.jpg' image)
- hovered item has to be highlighted also (#1 in the 'dropdown-screen.jpg' image)
- if there is no items with 'isSelected' set to 'true', then dropdown should show 'title' property as selected text (#2 in the 'dropdown-screen.jpg' image),
- when user changes selected value in dropdown, then 'onSelectedValueChanged' callback should be called,
- the dropdown popup should be closed when:
    * user clicks outside of the dropdown (#3 in the 'dropdown-screen.jpg' image)
    * user selects item in the dropdown (#4 in the 'dropdown-screen.jpg' image)
    * user clicks on the dropdown toggle element (#5 in the 'dropdown-screen.jpg' image)


 CSS:
 Please write css according to the SMACSS naming convention:
 .moduleName - camel case (.dropdown)
 .moduleName--subComponent - with double hyphen (.dropdown--item)
 .moduleName-is-opened - describes state of the module (.dropdown-is-opened)
 .moduleName--subComponent-is-selected - describes state of the sub component (.dropdown--item-is-selected)