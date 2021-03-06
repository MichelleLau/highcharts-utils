# Highcharts Utilities

Visual testing and debugging tools for Highcharts.

## Setup

 * OSX: `sudo node server`
 * Windows: Open a CLI with administrator priviliges and run `node server`

This will start a proxy server on port 80, start servers on `localhost:3030` and
`localhost:3031` (configurable ports) and set up virtual hosts for
`utils.highcharts.local` and `code.highcharts.local` respectively.

#### Unobtrusive utils
If you don't want to block port 80 and don't need the virtual hosts, run
`npm start` and open `http://localhost:3030`.

#### Debugging the utils application
Run `npm start` and open `http://localhost:3030`.


### Using with HTTPS

Enabling HTTPS makes it easier to test things on 3rd party pages that use SSL.

#### OSX

Run `cd certs && chmod 755 osx.create.ssl.certs.sh && ./osx.create.ssl.certs.sh` from the project directory. Requires that homebrew is installed.


Next you need to whitelist the certificate. Open the cert folder, and double click the `highcharts.local.csr`, and add it to the login keychain.
Note that the change only takes effect after the next system login.

#### Windows
Run `cd certs && ./win.create.ssl.certs.sh` from the project directory. Requires that OpenSSL is installed.
Press `Enter` to use the suggested default values for the certificate.

Next you need to install the certificate to whitelist it. Open the cert folder, and double click the `highcharts.local.csr`, select "Install Certficate...", and select "Next" until finished to let Windows choose the default settings.
Note that the change only takes effect after the next system login.

## Usage
See [highcharts/samples](https://github.com/highcharts/highcharts/tree/master/samples)
for description of how the samples are set up and how to use the utils.
