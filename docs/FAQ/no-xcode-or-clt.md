# The solution for Mac gyp: No Xcode or CLT version detected! error

Related Issue:

[TypeError: Cannot read property 'get' of undefined · Issue #108 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/108)

Please refer to this link for the solution: https://segmentfault.com/a/1190000021394623

When your Terminal displays such errors in the following:

- `Cannot find module '../build/Release/sharp.node'`
  - Solution: `npm install sharp --unsafe-perm`
- `Generating development SSR bundle failed \n Can't resolve 'prop-types'`
  - Solution: `npm install prop-types --save`
- `Type Error: Cannot read property 'get' of undefined`
  - Solution #1: reinstall Xcode
    - Uninstall `CommandandLineTools`
      - `sudo rm -rf $(xcode-select -p)`
    - Reinstall
      - `sudo xcode-select --install`

