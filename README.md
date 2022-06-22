## Material Design

**Material Design** is a design standard for ceating and designing websites and apps. Material design was introduced to bring order and unity to web design.

Material design concept was inspired by paper and ink in the physical world.As paer exists in three dimensions having shadows, folds and can be cut and resized - same goes for material design. It removed flat UI's with three dimensions designs.

**Examples of Material Design:**

<img src="screenshots/materialDesign1.jpg" width="200" height="100">
<img src="screenshots/materialDesign2.png" width="200" height="100">

## Radio Button

A radio button is a component used to select only one option from a predefined set of options, therefore it is also called as ***option button***.

Radio buttons are used where users need to select only one option out of 2 or more options. These options contain circular white space. If any option is selected then circular white space is getting filled with a dot.
If any option is already selected and you will click on any other option then the first option will be deselected.

In the image below **One** is *selected*, **Two** & **Three** are *deselected*.

<img src="screenshots/RadioButtonExample.png" width="100" height="100">

<hr/>

**Library Name:** Material Radio Button

**Library Version:** API 8 and above

**Library Release Date:** 06/06/2022

**Library Overview (Description):** This library is developed to provide material radio button/group implemented using extended typescript.

**GitHub link:** [https://github.com/Applib-OpenHarmony/MeterialRadio](https://github.com/Applib-OpenHarmony/MeterialRadio)

<hr/>

## Download & Install:

Install using npm: 
```
npm i ohos-material-radio
```

Details about OpenHarmony NPM environment configuration, click [here](https://gitee.com/openharmony-tpc/docs/blob/master/OpenHarmony_npm_usage.md). 

<hr/>

## Usage Instructions:

1. Import files and code dependencies

```ets
import { RadioButton, RadioGroup, RadioOption, RadioModel }  from '@ohos/material-radio'
```

2. Initialize model data

```
private radioModel: RadioModel = new RadioModel(1, "Radio Label")
```

3. Code for creating radio button

```
RadioButton({
    checked: true,
    model: this.radioModel,
    onCheckChange: (selectedRadioId) => {
        console.log("Selected Radio Button Id:: " + selectedRadioId);
    }
})
```

<img src="screenshots/Radio%20Buttons.png" width="300" height="500">

4. Code for creating radio group

```
RadioGroup(
    {
        selectedRadioId: 1,
        options: [new RadioOption(1, "Option 1"), new RadioOption(2, "Option 2")],
        onCheckChange: (selectedRadioId) => {
            console.log("Selected Radio Button Id:: " + selectedRadioId);
        }
    }
)
```

<img src="screenshots/Radio%20Group.png" width="300" height="500">

<hr/>

## Library Features:

### Feature-1: 

***Description:*** User needs to provide radioId, radiolabel, selectedRadioId to create material radio button. Apart from those user can also send checked and disabled properties also.

***Code Snippet:***

```
RadioButton({
    radioId: 1,
    radioLabel: $r('app.string.radio_button'),
    selectedRadioId: $selectedRadioId,
    checked: true,
    disabled: false,
    onSelect: (id) => {
        console.log(“Selected id:: “ + id)
    }
}) 
```

***Screenshot:***

<img src="screenshots/feature-1.jpg" width="300" height="400">

<br>

### Feature-2: 

***Description:*** User needs to provide radio options list to create material radio group.

***Code Snippet:***

```
RadioGroup({
    options: this.radioOptions,
    selectedRadioId: $selectedRadioId,
    onSelect: (id) => {
        console.log("Selected radio button id - " + id)
    }
}) 

```

***Screenshot:***

<img src="screenshots/feature-2.jpg" width="300" height="500">

<hr/>

## Conclusion:
This library is useful for providing material designs effects in radio button/group components. We can also give other specification like whether radio button is checked, disabled and a callback function to listen for changes on the radio button check status.

<hr/>

## Code Contribution:
If you find any problems during usage, you can submit an [Issue](https://github.com/Applib-OpenHarmony/MeterialRadio/issues) to us. Of course, we also welcome you to send us [PR](https://github.com/Applib-OpenHarmony/MeterialRadio/pulls).

<hr/>

## Reference:

**Designed by:** Dharma Seelan
