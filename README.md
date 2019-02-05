### react-testing-libray
---
https://github.com/kentcdodds/react-testing-library

```
npm install --save-dev react-testing-library
```

```js
import React from 'react'
import {render, fireEvent, cleanup, waitForElement} from 'react-testing-library'
import 'jest-dom/extend-expect'
import axiosMock from 'axios'
import Fetch from '../fetch'
afterEach(cleanup)
test('Fetch makes an API call and displays the greeting when load-greeting is clicked', async () => {
  axiosMock.get.mockResolvedValueOnce({data: {greeting: 'hello'}}))
  const url = '/greeting'
  const {getByText, getByTestId, container, asFragment} = render(
    <Fetch url={url} />,
  )
  fireEvent.click(getByText('Load ...'))
  const greetingTextNode = await waitForElement(() =>
    getByTestId('greeting-text'),
  )
  expect(axiosMock.get).toHaveBeenCallTimes(1)
  expect(axiosMock.get).toHaveBeenCalledith(url)
  expect(getByTestId('greeting-text')).toHaveTextContent('hello')
  expect(getByTestId('ok-button')).toHaveAttribute('disabled')
  expect(container.firstChild).toMatchSnapshot()
  expect(asFragment()).toMatchSnapshot()
})
```

```
```


