### react-testing-libray
---
https://github.com/kentcdodds/react-testing-library

```
npm install --save-dev react-testing-library
```

```js
import React from 'react'
import {} from ''
import ''
import axiosMock from ''
import Fetch from ''
afterEach()
test('', ({
  axiosMock.get.mockResolvedValueOnce({data: {greeting: 'hello'}}))
  const url = '/greeting'
  const {} = render(
    <Fetch url={url} />,
  )
  fireEvent.click(getByText(''))
  const greetingTextNode = await waitForElement(() =>
    getByTestId('greeting-text'),
  )
  expect(axiosMock.get).toHaveBeenCallTimes(1)
  expect(axiosMock.get).toHaveBeenCalledith(url)
  expect(getByTestId('greeting-text')).toHaveTextContent('hello')
  expect(container.firstChild).toMatchSnapshot()
  expect(asFragment()).toMatchSnapshot()
})
```

```
```


