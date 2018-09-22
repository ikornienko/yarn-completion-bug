The purposes of this repo is to provide a reproducible example for dsifford/yarn-completion#19.

### Environment

```bash
$ echo "bash: ${BASH_VERSINFO[*]}" ::: "bash-completion: ${BASH_COMPLETION_VERSINFO[*]}"
bash: 4 4 23 1 release x86_64-apple-darwin17.5.0 ::: bash-completion: 2 8
```

### How to Reproduce

There are several scenarios here:

1. `yarn test:`: press `tab` - completion does nothing, expected: it'll complete to `yarn test:some`
1. `yarn test:somet`: press `tab` - completion does nothing, expected: it'll complete to `yarn test:something`
1. `yarn test:some`: press `tab` twice - completion does nothing, expected: it'll offer `test:something` and `test:somemore`
1. `yarn test`: press `tab` - completion finishes it to `yarn test:some` as expected
