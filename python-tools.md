* Use watchdog to detect changes and run unit tests

```
pip3 install watchdog       # pip3 because I use Python3

# Basically runs the nose2 unittest everytime when it detects any changes to .py files
watchmedo shell-command -c 'clear; nose2 --config tests/unittest.cfg --verbose' -p '*.py' -R   
```