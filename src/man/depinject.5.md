# DEPINJECT 5 0.3

## NAME

depinject - Inject dependencies into third-party packages

## DESCRIPTION

leicht is a simple multipurpose Telegram bot that can handle and log direct messages or multi-user chat.

## CONFIGURATION

Put your debian-control-like json config files into **/etc/depinject/conf.d/**. Here is an example of such file:

```
{
    "name": "Inject cowsay and screenfetch with lightspeed",
    "x-depinject": "lightspeed",
    "dependencies": [
        {
            "name": "screenfetch",
            "version": ">= 3.0"
        },
        {
            "name": "cowsay",
            "version": "any"
        }
    ]
}
```

This config injects *screenfetch*(version >= 3.0) and *cowsay*(any version) as dependencies(**dependencies** array) for *lightspeed*(**x-depinject** field) package.

## BUGS

Please send your bugreports here: https://github.com/Like-all/depinject/issues

## AUTHOR

Written by Azer Abdullaev aka Like-all

## SEE ALSO

apt.conf(5)
