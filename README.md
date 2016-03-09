# WordPress Nav Menu
A WordPress navigation menu with checkboxes (for pure css dropdowns)

## Usage
Add the walker class into the `wp_nav_menu()` function as below

```php
<?php require_once "/path/to/walker_with_checkboxes.php"; ?>
<nav class="mobile-nav">
    <input type="checkbox" name="mobile-nav" id="mobile-nav" class="burger-check nav-check" />
    <label for="mobile-nav" class="burger white" tabindex="0">
        <span class="anim"></span>
        <span class="label-text">Open and close menu</span>
    </label>
    <?php
        wp_nav_menu(
            array(
                'theme_location' => 'main-navigation',
                'walker' => new Walker_With_Checkboxes()
            )
        );
    ?>
</nav>
```

## Additional Information
[`nav.css`](../master/nav.css) was crafted to accompany this to give some appropriate styling, but this can be some custom css

It is also recommended to add in [`waves.css`](../master/waves.css) and [`waves.min.js`](../master/waves.min.js) in order to get a nice click effect as the walker comes with the `waves-effect` css class on the relevant elements
