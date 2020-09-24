# Testing React Components

In order to test React components, you will need to create a file for each component in the format of `componentName.test.jsx`. To run all tests in your project, from your terminal enter `npm test`. The number of tests will be shown with how many passed and how many failed.

## NPM Testing Packages

These two packages will allow you to do additional testing. 
- `npm install react-test-renderer`
- `npm install enzyme`

## Smoke Tests

Smoke tests are test that check if the component renders correctly

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
import { shallow }, from 'enzyme';
import TestComp from './TestComp';

it('testing if the TestComp component loads', () => {
  const container = document.createElement( 'div' );
  ReactDOM.render( <TestComp />, container );
  ReactDOM.unmountComponentAtNode( container );
})
```

## Snapshot Tests

Snapshot tests if everything loads properly within a component

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
import { shallow }, from 'enzyme';
import TestComp from './TestComp';

it('testing that the elements load inside the TestComp', () => {
  const container = renderer.create(<BookForm />.toJSON();
  expect(container).toMatchSnapshot();
})
```

## Enzyme Tests

Enzyme tests see if the functionality of an event handler is working properly

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
import { shallow }, from 'enzyme';
import Tabs from './Tabs';

it('closes the first tab and opens any clicked tab', () => {
  const wrapper = shallow(<Tabs tabs={tabsProp} />)
  wrapper.find('button').at(1).simulate('click')
  expect(toJson(wrapper)).toMatchSnapshot()
})
```

