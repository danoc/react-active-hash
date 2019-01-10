# react-active-hash

[![Build status](https://badgen.net/travis/danoc/react-active-hash)](https://travis-ci.com/danoc/react-active-hash) [![Code coverage](https://badgen.net/codecov/c/github/danoc/react-active-hash)](https://codecov.io/gh/danoc/react-active-hash)

## Usage example

```jsx
import { HashContainer, HashLink, HashSection } from "react-hash";

const Page = () => (
  <HashContainer>
    <nav>
      <HashLink id="overview">
        {({ isActive, href, onClick }) => (
          <a href={href} onClick={onClick}>
            Overview
          </a>
        )}
      </HashLink>
      <HashLink id="history">
        {({ isActive, href, onClick }) => (
          <a href={href} onClick={onClick}>
            History
          </a>
        )}
      </HashLink>
    </nav>
    <main>
      {/*
        Generates a `div` with an `id` of overview. It accepts
        all attributes as well as an `is` prop that can be used
        to change the element.
      */}
      <HashSection id="overview">
        <h2>Overview</h2>
        <p>…</p>
      </HashSection>

      <HashSection id="history">
        <h2>History</h2>
        <p>…</p>
      </HashSection>
    </main>
  </HashContainer>
);
```
