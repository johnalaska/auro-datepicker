<!-- AURO-GENERATED-CONTENT:START (FILE:src=./../api.md) -->
<!-- The below content is automatically added from ./../api.md -->

# auro-datepicker

## Properties

| Property                          | Attribute                         | Type      | Default                                          | Description                                      |
|-----------------------------------|-----------------------------------|-----------|--------------------------------------------------|--------------------------------------------------|
| [centralDate](#centralDate)                     | `centralDate`                     | `String`  |                                                  | The date that determines the currently visible month. |
| [disabled](#disabled)                        | `disabled`                        | `Boolean` | false                                            | If set, disables the datepicker.                 |
| [error](#error)                           | `error`                           | `String`  |                                                  | When defined, sets persistent validity to `customError` and sets `setCustomValidity` = attribute value. |
| [maxDate](#maxDate)                         | `maxDate`                         | `String`  |                                                  | Maximum date. All dates after will be disabled.  |
| [minDate](#minDate)                         | `minDate`                         | `String`  |                                                  | Minimum date. All dates before will be disabled. |
| [monthNames](#monthNames)                      | `monthNames`                      | `array`   | ["January","February","March","April","May","June","July","August","September","October","November","December"] |                                                  |
| [noValidate](#noValidate)                      | `noValidate`                      | `Boolean` | false                                            | If set, disables auto-validation on blur.        |
| [range](#range)                           | `range`                           | `Boolean` | false                                            | If set, turns on date range functionality in auro-calendar. |
| [required](#required)                        | `required`                        | `Boolean` | false                                            | Populates the `required` attribute on the input. Used for client-side validation. |
| [setCustomValidity](#setCustomValidity)               | `setCustomValidity`               | `String`  |                                                  | Sets a custom help text message to display for all validityStates. |
| [setCustomValidityRangeOverflow](#setCustomValidityRangeOverflow)  | `setCustomValidityRangeOverflow`  | `String`  |                                                  | Custom help text message to display when validity = `rangeOverflow`. |
| [setCustomValidityRangeUnderflow](#setCustomValidityRangeUnderflow) | `setCustomValidityRangeUnderflow` | `String`  |                                                  | Custom help text message to display when validity = `rangeUnderflow`. |
| [setCustomValidityValueMissing](#setCustomValidityValueMissing)   | `setCustomValidityValueMissing`   | `String`  |                                                  | Help text message to display when validity = `valueMissing`; |
| [validity](#validity)                        | `validity`                        | `String`  | "undefined"                                      | Specifies the `validityState` this element is in. |
| [value](#value)                           | `value`                           | `String`  | "undefined"                                      | Value selected for the date picker.              |
| [valueEnd](#valueEnd)                        | `valueEnd`                        | `String`  | "undefined"                                      | Value selected for the second date picker when using date range. |

## Methods

| Method  | Type       | Description                         |
|---------|------------|-------------------------------------|
| [focus](#focus) | `(): void` | Focuses the combobox trigger input. |

## Events

| Event                      | Type                              | Description                                      |
|----------------------------|-----------------------------------|--------------------------------------------------|
| `auroDatePicker-ready`     | `CustomEvent<any>`                | Notifies that the component has finished initializing. |
| `auroDatePicker-valueSet`  |                                   | Notifies that the component has a new value set. |
| `auroDatepicker-validated` | `CustomEvent<{ validity: any; }>` | Notifies that the component value(s) have been validated. |

## Slots

| Name              | Description                                      |
|-------------------|--------------------------------------------------|
| [fromLabel](#fromLabel)       | Defines the label content for the first input.   |
| [helpText](#helpText)        | Defines the content of the helpText.             |
| [mobileDateLabel](#mobileDateLabel) | Defines the content to display above selected dates in the mobile layout. |
| [toLabel](#toLabel)         | Defines the label content for the second input when the `range` attribute is used. |
<!-- AURO-GENERATED-CONTENT:END -->

## API Examples

### Basic

<div class="twoColDemoRow">
  <div>
    <div class="exampleWrapper">
      <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/basic.html) -->
      <!-- The below content is automatically added from ./../../apiExamples/basic.html -->
      <auro-datepicker>
        <span slot="fromLabel">Choose a date</span>
        <span slot="mobileDateLabel">Choose a date</span>
      </auro-datepicker>
      <!-- AURO-GENERATED-CONTENT:END -->
    </div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/basic.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/basic.html -->

```html
<auro-datepicker>
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

### Property Examples

#### centralDate

Date that determines the currently visible month.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/centralDate.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/centralDate.html -->
  <auro-datepicker centralDate="06/16/1980">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/centralDate.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/centralDate.html -->

```html
<auro-datepicker centralDate="06/16/1980">
  <span slot="label">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### disabled

If set, disables the datepicker.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/disabled.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/disabled.html -->
  <auro-datepicker disabled>
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/disabled.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/disabled.html -->

```html
<auro-datepicker disabled>
  <span slot="label">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### error

Sets a persistent error state (e.g. an error state returned from the server). This error state will override all default validation until the error attribute is removed from the datepicker.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/error.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/error.html -->
  <auro-datepicker error="Custom error message" id="errorExample">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <br/><br/>
  <auro-button id="undefinedValueExampleBtnAddError">Set Error</auro-button>
  <auro-button id="undefinedValueExampleBtnRemoveError">Remove Error</auro-button>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/error.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/error.html -->

```html
<auro-datepicker error="Custom error message" id="errorExample">
  <span slot="label">Choose a date</span>
</auro-datepicker>
<br/><br/>
<auro-button id="undefinedValueExampleBtnAddError">Set Error</auro-button>
<auro-button id="undefinedValueExampleBtnRemoveError">Remove Error</auro-button>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### maxDate

To give a higher limit you can bind a date to the `maxDate` property. It is recommended to use the `setCustomValidityRangeOverflow` attribute to define an error message to display when validation fails the maximum date restriction.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/maxDate.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/maxDate.html -->
  <auro-datepicker maxDate="03/25/2023" setCustomValidityRangeOverflow="Selected date is later than maximum date.">
    <span slot="fromLabel">Choose a date</span>
    <span slot="mobileDateLabel">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/maxDate.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/maxDate.html -->

```html
<auro-datepicker maxDate="03/25/2023" setCustomValidityRangeOverflow="Selected date is later than maximum date.">
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>
Setting the `maxDate` attribute to a date earlier than the auro-datepicker `value` will result in the following changes to the component state:

* `value` will to reset to `undefined`.
* If the currently viewed calendar month is later than the new `maxDate`, the calendar view will move to the new `maxDate` month.

This example demonstrates that behavior.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/updateMaxDate.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/updateMaxDate.html -->
  <auro-datepicker id="maxDateExample" setCustomValidityRangeOverflow="Selected date is later than maximum date.">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <auro-button id="maxDateChange">Change maxDate to Today's Date</auro-button>
  <auro-button id="resetMaxDate">Reset Datepicker to Initial Example</auro-button>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/updateMaxDate.js) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/updateMaxDate.js -->

```js
function formatDateString(date) {
  /* eslint-disable prefer-template, no-magic-numbers */
  const dd = String("0" + date.getDate()).slice(-2);
  const mm = String("0" + (date.getMonth() + 1)).slice(-2);
  /* eslint-enable prefer-template, no-magic-numbers */
  const yyyy = date.getFullYear();

  return `${mm}/${dd}/${yyyy}`;
}

export function updateMaxDateExample() {
  const maxDateExample = document.getElementById('maxDateExample');
  const changeMaxDateButton = document.getElementById('maxDateChange');
  const resetButton = document.getElementById('resetMaxDate');

  const today = formatDateString(new Date());

  let nextWeek = new Date();
  let addOneWeek = nextWeek.getDate() + 7;

  nextWeek.setDate(addOneWeek);
  nextWeek = formatDateString(nextWeek);

  maxDateExample.setAttribute('value', nextWeek);
  maxDateExample.setAttribute('maxDate', nextWeek);

  changeMaxDateButton.addEventListener('click', () => {
    maxDateExample.setAttribute('maxDate', today);
  });

  resetButton.addEventListener('click', () => {
    maxDateExample.setAttribute('value', nextWeek);
    maxDateExample.setAttribute('maxDate', nextWeek);
  });
}
```
<!-- AURO-GENERATED-CONTENT:END -->
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/updateMaxDate.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/updateMaxDate.html -->

```html
<auro-datepicker id="maxDateExample" setCustomValidityRangeOverflow="Selected date is later than maximum date.">
  <span slot="label">Choose a date</span>
</auro-datepicker>
<auro-button id="maxDateChange">Change maxDate to Today's Date</auro-button>
<auro-button id="resetMaxDate">Reset Datepicker to Initial Example</auro-button>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### minDate

To give a lower limit you can bind a date to the `minDate` property. It is recommended to use the `setCustomValidityRangeUnderflow` attribute to define an error message to display when validation fails the minimum date restriction.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/minDate.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/minDate.html -->
  <auro-datepicker minDate="03/25/2028" setCustomValidityRangeUnderflow="Selected date is earlier than the minimum date.">
    <span slot="fromLabel">Choose a date</span>
    <span slot="mobileDateLabel">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/minDate.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/minDate.html -->

```html
<auro-datepicker minDate="03/25/2028" setCustomValidityRangeUnderflow="Selected date is earlier than the minimum date.">
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>
Setting the `minDate` attribute to a date later than the auro-datepicker `value` will result in the following changes to the component state:

* `value` will to reset to `undefined`.
* If the currently viewed calendar month is earlier than the new `minDate`, the calendar view will move to the new `minDate` month.

This example demonstrates that behavior.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/updateMinDate.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/updateMinDate.html -->
  <auro-datepicker id="minDateExample" setCustomValidityRangeUnderflow="Selected date is earlier than the minimum date.">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <auro-button id="minDateChange">Change minDate to a week from Today</auro-button>
  <auro-button id="resetMinDate">Reset Datepicker to Initial Example</auro-button>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/updateMinDate.js) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/updateMinDate.js -->

```js
function formatDateString(date) {
  /* eslint-disable prefer-template, no-magic-numbers */
  const dd = String("0" + date.getDate()).slice(-2);
  const mm = String("0" + (date.getMonth() + 1)).slice(-2);
  /* eslint-enable prefer-template, no-magic-numbers */
  const yyyy = date.getFullYear();

  return `${mm}/${dd}/${yyyy}`;
}

export function updateMinDateExample() {
  const minDateExample = document.getElementById('minDateExample');
  const changeMinDateButton = document.getElementById('minDateChange');
  const resetButton = document.getElementById('resetMinDate');

  const today = formatDateString(new Date());

  let nextWeek = new Date();
  let addOneWeek = nextWeek.getDate() + 7;

  nextWeek.setDate(addOneWeek);
  nextWeek = formatDateString(nextWeek);

  minDateExample.setAttribute('value', today);
  minDateExample.setAttribute('minDate', today);

  changeMinDateButton.addEventListener('click', () => {
    minDateExample.setAttribute('minDate', nextWeek);
  });

  resetButton.addEventListener('click', () => {
    minDateExample.setAttribute('value', today);
    minDateExample.setAttribute('minDate', today);
  });

}
```
<!-- AURO-GENERATED-CONTENT:END -->
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/updateMinDate.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/updateMinDate.html -->

```html
<auro-datepicker id="minDateExample" setCustomValidityRangeUnderflow="Selected date is earlier than the minimum date.">
  <span slot="label">Choose a date</span>
</auro-datepicker>
<auro-button id="minDateChange">Change minDate to a week from Today</auro-button>
<auro-button id="resetMinDate">Reset Datepicker to Initial Example</auro-button>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### monthNames

May be used to provide localized month names. These names will only be shown in the calendar when viewed on a mobile device.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/monthNames.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/monthNames.html -->
  <auro-datepicker id="monthNamesExample">
    <span slot="fromLabel">Choose a date</span>
    <span slot="mobileDateLabel">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/monthNames.js) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/monthNames.js -->

```js
export function monthNamesExample() {
  const monthNamesExample = document.querySelector('#monthNamesExample');
  const spanishMonths = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'];

  monthNamesExample.monthNames = spanishMonths;
}
```
<!-- AURO-GENERATED-CONTENT:END -->
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/monthNames.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/monthNames.html -->

```html
<auro-datepicker id="monthNamesExample">
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### noValidate

When set, the datepicker will not validate when navigating away from the component.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/noValidate.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/noValidate.html -->
  <auro-datepicker required noValidate>
    <span slot="fromLabel">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/noValidate.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/noValidate.html -->

```html
<auro-datepicker required noValidate>
  <span slot="fromLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### range

When used, the datepicker will display two inputs and the component will support selection of dates for a start and end date.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/basicRange.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/basicRange.html -->
  <auro-datepicker range>
    <span slot="fromLabel">Departure</span>
    <span slot="toLabel">Return</span>
    <span slot="mobileDateLabel">Roundtrip</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/basicRange.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/basicRange.html -->

```html
<auro-datepicker range>
  <span slot="fromLabel">Departure</span>
  <span slot="toLabel">Return</span>
  <span slot="mobileDateLabel">Roundtrip</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### required

Populates the `required` attribute on the input. Used for client-side validation.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/required.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/required.html -->
  <auro-datepicker required setCustomValidityValueMissing="Custom value missing message.">
    <span slot="fromLabel">Choose a date</span>
    <span slot="mobileDateLabel">Choose a date</span>
  </auro-datepicker>
  <auro-datepicker required range setCustomValidityValueMissing="Custom value missing message.">
    <span slot="fromLabel">Departure</span>
    <span slot="toLabel">Return</span>
    <span slot="mobileDateLabel">Roundtrip</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/required.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/required.html -->

```html
<auro-datepicker required setCustomValidityValueMissing="Custom value missing message.">
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
<auro-datepicker required range setCustomValidityValueMissing="Custom value missing message.">
  <span slot="fromLabel">Departure</span>
  <span slot="toLabel">Return</span>
  <span slot="mobileDateLabel">Roundtrip</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### validity

Specifies the `validityState` the element is in. Upon first interaction, or presetting the `error` attribute, the component will validate on `focusout`. After validation, `validityState` can be queried from the component by using the following JavaScript.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/validity.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/validity.html -->
  <auro-datepicker required id="validityExample">
    <span slot="fromLabel">Choose a date</span>
  </auro-datepicker>
  <auro-button id="validityExampleBtn">Get validity</auro-button>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/validity.js) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/validity.js -->

```js
export function validityExample() {
  const validityExampleExample = document.querySelector('#validityExample');
  const validityExampleExampleBtn = document.querySelector('#validityExampleBtn');

  validityExampleExampleBtn.addEventListener('click', () => {
    console.warn('Validity set to:', validityExampleExample.validity);
    alert(`Validity set to: ${validityExampleExample.validity}`);
  })
}
```
<!-- AURO-GENERATED-CONTENT:END -->
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/validity.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/validity.html -->

```html
<auro-datepicker required id="validityExample">
  <span slot="fromLabel">Choose a date</span>
</auro-datepicker>
<auro-button id="validityExampleBtn">Get validity</auro-button>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### value

Value selected for the datepicker. Can be used to pre-set the value of the datepicker. When the `range` attribute is used, `value` is for the first input.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/value.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/value.html -->
  <auro-datepicker id="valueExample" value="02/02/2022">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/value.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/value.html -->

```html
<auro-datepicker id="valueExample" value="02/02/2022">
  <span slot="label">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### valueEnd

Value of the second input (end date), selected for the datepicker. Can be used to pre-set the value of the datepicker. Only applicable for a datepicker with the `range` attribute.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/valueEnd.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/valueEnd.html -->
  <auro-datepicker id="valueEndExample" range valueEnd="03/03/2023">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/valueEnd.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/valueEnd.html -->

```html
<auro-datepicker id="valueEndExample" range valueEnd="03/03/2023">
  <span slot="label">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

### Method Examples

#### focus

The focus method will apply focus state to the datepicker's input field.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/focus.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/focus.html -->
  <auro-button id="focusExampleBtn">Apply focus to datepicker</auro-button>
  <br /><br />
  <auro-datepicker id="focusExample">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/focus.js) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/focus.js -->

```js
export function focusExample() {
  const focusExample = document.querySelector('#focusExample');
  const focusExampleBtn = document.querySelector('#focusExampleBtn');

  focusExampleBtn.addEventListener('click', () => {
    focusExample.focus();
  });
}
```
<!-- AURO-GENERATED-CONTENT:END -->
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/focus.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/focus.html -->

```html
<auro-button id="focusExampleBtn">Apply focus to datepicker</auro-button>
<br /><br />
<auro-datepicker id="focusExample">
  <span slot="label">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

### Slot Examples

#### fromLabel

Sets the label used for the input. When the `range` attribute is used this is the first of two inputs.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/basic.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/basic.html -->
  <auro-datepicker>
    <span slot="fromLabel">Choose a date</span>
    <span slot="mobileDateLabel">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/basic.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/basic.html -->

```html
<auro-datepicker>
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### helpText

Sets the help text displayed below the trigger. The `helpText` slot can be used to provide additional context for the combobox. When using the `error` property, the `helpText` slot can be used to describe the error.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/helpText.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/helpText.html -->
  <auro-datepicker>
    <span slot="label">Choose a date</span>
    <span slot="helpText">Choose a date must be today or earlier.</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/helpText.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/helpText.html -->

```html
<auro-datepicker>
  <span slot="label">Choose a date</span>
  <span slot="helpText">Choose a date must be today or earlier.</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### mobileDateLabel

Sets the label used for the selected date display at the top of the bib when viewed in the mobile layout. To view this demo, set your window to a mobile screen size.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/basic.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/basic.html -->
  <auro-datepicker>
    <span slot="fromLabel">Choose a date</span>
    <span slot="mobileDateLabel">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/basic.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/basic.html -->

```html
<auro-datepicker>
  <span slot="fromLabel">Choose a date</span>
  <span slot="mobileDateLabel">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

#### toLabel

Only for use with the `range` attribute. Sets the label for the second input.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/basicRange.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/basicRange.html -->
  <auro-datepicker range>
    <span slot="fromLabel">Departure</span>
    <span slot="toLabel">Return</span>
    <span slot="mobileDateLabel">Roundtrip</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/basicRange.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/basicRange.html -->

```html
<auro-datepicker range>
  <span slot="fromLabel">Departure</span>
  <span slot="toLabel">Return</span>
  <span slot="mobileDateLabel">Roundtrip</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>

## Functional Examples

### Watch for value changes

The following example listens for the `auroDatePicker-valueSet` event. Once triggered, `element.value` may be queried for the new value **and** in successful scenarios, an alert will appear. Open the JavaScript console in the browser's developer tools to see the `console.warn` message that appears after the `auroDatePicker-valueSet` event has been triggered.

<div class="exampleWrapper">
  <!-- AURO-GENERATED-CONTENT:START (FILE:src=./../../apiExamples/alertValue.html) -->
  <!-- The below content is automatically added from ./../../apiExamples/alertValue.html -->
  <auro-datepicker id="datePickerValueAlert">
    <span slot="label">Choose a date</span>
  </auro-datepicker>
  <!-- AURO-GENERATED-CONTENT:END -->
</div>
<auro-accordion lowProfile justifyRight>
  <span slot="trigger">See code</span>
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/alertValue.js) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/alertValue.js -->

```js
export function alertValueExample() {
  const valueAlertExample = document.querySelector('#datePickerValueAlert');

  valueAlertExample.addEventListener('auroDatePicker-valueSet', () => {
    console.warn('Select value changed to:', valueAlertExample.value);
    alert(`Select value changed to: ${valueAlertExample.value}`);
  })
}
```
<!-- AURO-GENERATED-CONTENT:END -->
<!-- AURO-GENERATED-CONTENT:START (CODE:src=./../../apiExamples/alertValue.html) -->
<!-- The below code snippet is automatically added from ./../../apiExamples/alertValue.html -->

```html
<auro-datepicker id="datePickerValueAlert">
  <span slot="label">Choose a date</span>
</auro-datepicker>
```
<!-- AURO-GENERATED-CONTENT:END -->
</auro-accordion>
