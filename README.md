[![Build Status](https://travis-ci.org/eduroom/eduroom-ui.svg?branch=master)](https://travis-ci.org/eduroom/eduroom-ui)


#### License ####

Every code patch accepted in taiga codebase is licensed under [AGPL v3.0](http://www.gnu.org/licenses/agpl-3.0.html). You must be careful to not include any code that can not be licensed under this license.

Please read carefully [our license](https://github.com/taigaio/taiga-front/blob/master/LICENSE) and ask us if you have any questions.

Emoji provided free by [Twemoji](https://github.com/twitter/twemoji)


#### Translation ####

We are ready now to accept your help translating Taiga. It's easy (and fun!) just access our team of translators with the link below, set up an account in Transifex and start contributing. Join us to make sure your language is covered! **[Help Taiga to translate content](https://www.transifex.com/signup/ "Help Taiga to translate content")**


#### Code patches ####

Taiga will always be glad to receive code patches to update, fix or improve its code.

If you know how to improve our code base or you found a bug, a security vulnerability or a performance issue and you think you can solve it, we will be very happy to accept your pull-request. If your code requires considerable changes, we recommend you first  talk to us directly. We will find the best way to help.

#### Initial dev env ####

Install requirements:

**Ruby / Sass**

You can install Ruby through the apt package manager, rbenv, or rvm.
Install Sass through your **Terminal or Command Prompt**.

```
gem install sass scss-lint
export PATH="~/.gem/ruby/2.1.0/bin:$PATH"
sass -v             # should return Sass 3.3.8 (Maptastic Maple)
```

Complete process for all OS at: http://sass-lang.com/install

**Node + Gulp**

We recommend using [nvm](https://github.com/creationix/nvm) to manage different node versions
```
npm install -g gulp
npm install
gulp
```

And go in your browser to: http://localhost:9001/

#### E2E test ####

If you want to run e2e tests

```
npm install -g protractor
npm install -g mocha
npm install -g babel@5

webdriver-manager update
```

To run a local Selenium Server, you will need to have the Java Development Kit (JDK) installed.

## Tests ##

#### Unit tests ####

- To run **unit tests**

  ```
  gulp
  ```
  ```
  npm test
  ```

#### E2E tests ####

- To run **e2e tests** you need [taiga-back](https://github.com/taigaio/taiga-back) running and

  ```
  gulp
  ```
  ```
  webdriver-manager start
  ```
  ```
  protractor conf.e2e.js --suite=auth     # To tests authentication
  protractor conf.e2e.js --suite=full     # To test all the platform authenticated
  ```
