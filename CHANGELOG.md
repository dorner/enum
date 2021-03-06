**1.7.0**
* `attr_enum` reader always returns an EnumValue.
* `EnumValue#t` uses `String#titlelize` if it's available and I18n or the
  specific translation are not available.

**1.7.1**
* Remove usage of `reverse_merge`, apparently doesn't exist in Ruby core.
* `attr_enum`'s writer does not pass an `EnumValue` to the super.
* Fix `EnumValue#t` specs (mocking `I18n`).

**1.7.2**
* Added `Object#enum_value?` to fix `attr_enum`'s writer, `BasicObject` does
  not have `respond_to?`.
* Fix specs that didn't catch above bug.

**1.7.3**
* `attr_enum`'s writer to accept empty string.
* `attr_enum`'s qualifier option to use the object's `#send` rather than `#[]`.

**1.7.4**
* `attr_enum`'s reader allows super to hold the name etc.
* Add `#attr_enum` and `#enum` only to modules and classes (not any instance).
