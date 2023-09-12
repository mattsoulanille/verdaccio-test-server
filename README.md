# verdaccio-test-server

A really simple repo to run and log into a local verdaccio server for ad-hoc testing.

## Usage

Run the following commands:
```bash
yarn
yarn start
```
Then, open http://localhost:5873 to check if it's running.

In another terminal, run the following to log in to the local verdaccio server:

```bash
yarn verdaccio-login
```

To delete all locally published packages, run the following:

```bash
yarn clean
```

You can now publish packages to this local repo. For TensorFlow.js specifically, the following command when run in the base of the tfjs repo will publish to this Verdaccio server.
```bash
yarn publish-npm --no-otp --registry http://127.0.0.1:5873
```
