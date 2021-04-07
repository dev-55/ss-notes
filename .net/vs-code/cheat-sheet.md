# Cheat Sheet

## Debug

To Debug with Command Line Arguments, add these to launch.json...
```
"args": [
    "-e", "localstack"
],
```
```
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python: <Any_Name>",
      "type": "python",
      "request": "launch",
      "program":"${file}"

      "args": [
        "-c", "/Users/xyz/config",
        "-p", "2012"
      ]
    }
  ]
}{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python: <Any_Name>",
      "type": "python",
      "request": "launch",
      "program":"${file}"

      "args": [
        "-c", "/Users/xyz/config",
        "-p", "2012"
      ]
    }
  ]
}
```