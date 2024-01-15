
## Configuration

To configure True for SCSS testing, you need to create a configuration file. Here's an example of a True configuration file for SCSS testing:

```javascript
// true.config.js
module.exports = {
  testMatch: ['**/*.scss'],
  // Add any additional configuration options here
};
```

You can customize the `testMatch` option to specify the file patterns for your SCSS tests.

## Writing SCSS Tests

To write SCSS tests with True, you need to create test files with the `.test.scss` extension. Here's an example of an SCSS test file:

```scss
// button.test.scss
@import 'button';

.test {
  @include test('Button should have correct background color', {
    background-color: #f00;
  });
}
```

In this example, we import the SCSS file we want to test and use the `test` mixin provided by True to define the test case.

## Running SCSS Tests

To run your SCSS tests, you can use the True CLI. Here's an example command to run all SCSS tests in your project:

```shell
npx true test
```

You can also specify a specific test file or directory to run:

```shell
npx true test path/to/test/file.test.scss
```

## Integration with Build Process

To incorporate SCSS testing into your build process, you can add a test script to your project's `package.json` file:

```json
{
  "scripts": {
    "test:scss": "true test"
  }
}
```

You can then run your SCSS tests as part of your build or CI/CD pipeline using the following command:

```shell
npm run test:scss
