>rails 4

To reset the binstubs, just delete your bin/ directory in rails and run:
```
#generates binstubs for ALL gems in the bundle
bundle install --binstubs

# ...OR, generate binstubs for a SINGLE gem (recommended)
bundle binstubs rake
```
>rails 5/rails 6
To reset the binstubs, just delete your bin/ directory in rails and run:
```
rake app:update:bin
```
