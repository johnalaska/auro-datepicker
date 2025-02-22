# auro-datepicker

## Properties

| Property                          | Attribute                         | Type      | Default                                          | Description                                      |
|-----------------------------------|-----------------------------------|-----------|--------------------------------------------------|--------------------------------------------------|
| `centralDate`                     | `centralDate`                     | `String`  |                                                  | The date that determines the currently visible month. |
| `disabled`                        | `disabled`                        | `Boolean` | false                                            | If set, disables the datepicker.                 |
| `error`                           | `error`                           | `String`  |                                                  | When defined, sets persistent validity to `customError` and sets `setCustomValidity` = attribute value. |
| `maxDate`                         | `maxDate`                         | `String`  |                                                  | Maximum date. All dates after will be disabled.  |
| `minDate`                         | `minDate`                         | `String`  |                                                  | Minimum date. All dates before will be disabled. |
| `monthNames`                      | `monthNames`                      | `array`   | ["January","February","March","April","May","June","July","August","September","October","November","December"] |                                                  |
| `noValidate`                      | `noValidate`                      | `Boolean` | false                                            | If set, disables auto-validation on blur.        |
| `range`                           | `range`                           | `Boolean` | false                                            | If set, turns on date range functionality in auro-calendar. |
| `required`                        | `required`                        | `Boolean` | false                                            | Populates the `required` attribute on the input. Used for client-side validation. |
| `setCustomValidity`               | `setCustomValidity`               | `String`  |                                                  | Sets a custom help text message to display for all validityStates. |
| `setCustomValidityRangeOverflow`  | `setCustomValidityRangeOverflow`  | `String`  |                                                  | Custom help text message to display when validity = `rangeOverflow`. |
| `setCustomValidityRangeUnderflow` | `setCustomValidityRangeUnderflow` | `String`  |                                                  | Custom help text message to display when validity = `rangeUnderflow`. |
| `setCustomValidityValueMissing`   | `setCustomValidityValueMissing`   | `String`  |                                                  | Help text message to display when validity = `valueMissing`; |
| `validity`                        | `validity`                        | `String`  | "undefined"                                      | Specifies the `validityState` this element is in. |
| `value`                           | `value`                           | `String`  | "undefined"                                      | Value selected for the date picker.              |
| `valueEnd`                        | `valueEnd`                        | `String`  | "undefined"                                      | Value selected for the second date picker when using date range. |

## Methods

| Method  | Type       | Description                         |
|---------|------------|-------------------------------------|
| `focus` | `(): void` | Focuses the combobox trigger input. |

## Events

| Event                      | Type                              | Description                                      |
|----------------------------|-----------------------------------|--------------------------------------------------|
| `auroDatePicker-ready`     | `CustomEvent<any>`                | Notifies that the component has finished initializing. |
| `auroDatePicker-valueSet`  |                                   | Notifies that the component has a new value set. |
| `auroDatepicker-validated` | `CustomEvent<{ validity: any; }>` | Notifies that the component value(s) have been validated. |

## Slots

| Name              | Description                                      |
|-------------------|--------------------------------------------------|
| `fromLabel`       | Defines the label content for the first input.   |
| `helpText`        | Defines the content of the helpText.             |
| `mobileDateLabel` | Defines the content to display above selected dates in the mobile layout. |
| `toLabel`         | Defines the label content for the second input when the `range` attribute is used. |
