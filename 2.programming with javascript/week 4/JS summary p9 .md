## `Jest testing`

1. Set Up Jest:

+ Install Jest:
wite the command in termianl of VScode or your text editor
``````
npm install --save-dev jest
``````
+ Configure Jest by adding a jest.config.js file or "jest" section in your package.json:

``````
// package.json
{
  "jest": {
    "testMatch": ["**/__tests__/**/*.test.js"]
  }
}
``````
2. Create Test Files:

    Organize tests in a directory (e.g., __tests__).
    Name test files with a .test.js extension (e.g., myModule.test.js).
3. Write Test Cases:

``````js
// myModule.test.js
const add = require('./myModule');

test('Adding 1 + 2 should equal 3', () => {
  // Arrange
  const a = 1;
  const b = 2;

  // Act
  const result = add(a, b); // Assume there's an 'add' function.
  
  // Assert
  expect(result).toBe(3);
});
``````
4. Assertions:

Use Jest's assertion functions in your test cases:

``````js
expect(value).toBe(expected);
expect(value).toEqual(expected);
expect(value).toBeTruthy();
expect(value).toBeFalsy();
expect(value).toMatch(pattern);
expect(value).toContain(item);
``````
5. Run Tests:

Execute tests with the jest command:

``````
npx jest
``````
