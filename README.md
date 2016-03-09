# WordPress Nav Menu
A WordPress navigation menu with checkboxes (for pure css dropdowns)

## Usage
Add the walker class into the ```wp_nav_menu()``` function as below

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
