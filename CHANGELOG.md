# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-translate`, published as `gizmocraft/zendframework1-translate`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-translate` to `gizmocraft/zendframework1-translate`. It now requires `gizmocraft/zendframework1-exception` `^2.0.0`, `gizmocraft/zendframework1-config` `^3.0.0`, `gizmocraft/zendframework1-loader` `^2.0.0`, `gizmocraft/zendframework1-xml` `^2.0.0`, `gizmocraft/zendframework1-cache` `^2.0.0`, `gizmocraft/zendframework1-locale` `^2.0.0` and `gizmocraft/zendframework1-log` `^2.0.0`.

### Other changes

- No public signature changes.
- `Zend_Translate_Adapter_Array`, `Zend_Translate_Adapter_Ini` and `Zend_Translate_Adapter::addTranslation()` no longer pass strings containing NUL bytes to `file_exists()`/`is_dir()`, which throw a `ValueError` on PHP 8.6. Array and Ini data with a NUL byte now end in the usual `Zend_Translate_Exception`.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. Two tests added for the NUL byte handling.
- Removed two obsolete PHPStan ignore patterns.
- CI runs PHP 8.5 and 8.6.
