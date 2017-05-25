// Your recommended changes go here

## Visual to the UI (CSS, visual elements)
- There is a loss of visual focus when tabbing through the top line items. After the 'Skip Navigation' button, the first four links (Healthcare.gov, Individuals & Families, Small Businesses, and Log in) provide no visual indication that these elements are currently selected by the tab function until you reach the 'Espanol' button.

- SELECT buttons should go full-width horizontal on small screen resolutions (lowest breakpoint in your CSS), both to match the behavior of the REMOVE buttons and to make them easier to click when using touchscreens.

## Technical changes: HTML, CSS, Javascript, ARIA attributes
- REMOVE buttons contain no unique name property to associate them with the element they remove. Button code lacks unique identifiers:
<button class="btn btn-block btn-sm" ng-click="removeCoverable(coverableType, coverable)">
                    Remove
                  </button>
              
- When viewed without CSS, the page contains two Healthcare.gov logos (this also comes up when tabbing through), as well as two sets of top navigation menu items (Individuals & Families, Small Businesses, Log in, Espanol). Several error messages and some hidden content are also revealed on the page, which may cause confusion to users viewing on devices or software without stylesheet support.

## Content
- Item removal happens automatically with one click. An 'Are You Sure?' dialog would be a good feature.
