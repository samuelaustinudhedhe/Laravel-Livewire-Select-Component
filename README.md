# Laravel Livewire Select Component

![Livewire Version 3](https://laravel-livewire.com/img/logo.svg)

## Description

The **Laravel Livewire Select Component** is a custom component designed to enhance the functionality of HTML `<select>` elements when used with Laravel Livewire. This component seamlessly integrates with Livewire to manage the default selected state of options, ensuring compatibility with Livewire's reactivity. It allows for programmatic default option selection and optimizes performance through an optional JavaScript loading feature.

## Compatibility

- **Laravel**: 11.x
- **Livewire**: 3.x
- **PHP**: 8.3

## Features

- **Dynamic Default Option Management**: Automatically selects the first option or an option defined by the `selected` attribute if no value is set in Livewire.
- **`loadJS` Feature**: Provides control over loading JavaScript functionality for managing default options dynamically, improving performance in forms with multiple select inputs.
- **Integration with Livewire**: Ensures that the selected state of the `<select>` element stays in sync with Livewire models, even in complex nested structures.
- **Custom Styling**: Includes pre-defined utility classes for responsive and accessible design, easily customizable via the `class` attribute.

## Installation

1. Create a new Blade component by creating a file named `select.blade.php` in your `resources/views/components` directory.
2. Copy the entire contents of the `x-select` component code into your newly created `select.blade.php` file.

## How to Use the Component

To use the Laravel Livewire Select Component, include it in your Blade views as follows:

```blade
<form>
    <!-- Only load JS on one select per Blade file or per page -->

    <!-- Use the 'defaultValue' custom attribute to set the default value of the select -->
    <x-select loadJS="true" wire:model="formData.option1" defaultValue="1">
        <option value="">--Select Option 1--</option>
        <option value="1">Option 1</option>
        <option value="2">Option 2</option>
    </x-select>

    <!-- Automatically picks the first option as the default value of the select -->
    <x-select wire:model="formData.option2">
        <option value="">--Select Option 2--</option>
        <option value="A">Option A</option>
        <option value="B">Option B</option>
    </x-select>

    <!-- Picks the option with the 'selected' attribute as the default value of the select -->
    <x-select wire:model="formData.option3">
        <option value="">--Select Option 3--</option>
        <option value="i">Option i</option>
        <option selected value="ii">Option ii</option>
    </x-select>
</form>
```

## Use Cases
- **Forms with Single and Multiple Select Inputs**: This component simplifies managing multiple <select> inputs in a form, especially when they are nested within arrays.
- **Handling Initial States**: Ideal when you need to set an initial value for <select> elements programmatically, while still allowing Livewire to handle dynamic updates.
- **Avoiding Livewire's DOM Morph Issues**: Prevents Livewire from resetting or overriding the selected state during DOM updates.


## Contributions
Contributions to this component are welcome! If you find any bugs or have feature requests, feel free to submit an issue or a pull request.

## License
This component is open-source and available under the MIT License. See the LICENSE file for more details.

Feel free to adjust any sections to better fit your style or project needs! Let me know if there are any other details you want to include.