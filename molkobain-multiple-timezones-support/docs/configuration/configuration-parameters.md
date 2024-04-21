<button onclick="history.back()">Back</button>

# Configuration parameters

No initial configuration needed, each user will be prompt to choose its timezone on next login.

Some configuration parameters are available though for fine-tuning:

  * `enabled` Enable / disable the extension without having to uninstall it. Value can be `true` or `false`.
  * `disabled_guis` Specify for which GUIs the extension should be disabled, for example if you only want to use it in the backoffice and not in the end-users portal. Values can be `backoffice`, `itop-portal` or any other portal instance ID.

*Default values:*
```
'molkobain-multiple-timezones-support' => array(
    'enabled' => true,
    'disabled_guis' => array(),
),
```
