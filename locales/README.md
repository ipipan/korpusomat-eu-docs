# In order to translate .rst files follow below steps:
<br>

## Generate .pot files from source
```sphinx-build -b gettext docs/source docs/source/_build/gettext```

## Update .po files for English (or any language)
```sphinx-intl update -p docs/source/_build/gettext -l en```

## Compile .mo files from .po files
```
for f in locales/en/LC_MESSAGES/*.po; do
    msgfmt "$f" -o "${f%.po}.mo"
done
```

## Build the English html documentation to see translated html
```sphinx-build -b html -D language='en' docs/source docs/_build/en```

