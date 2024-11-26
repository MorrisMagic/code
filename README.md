# code1

import React from 'react';

interface GreetingProps {
  name: string; // 'name' should be of type 'string'
}

const Greeting: React.FC<GreetingProps> = ({ name }) => {
  return <div>Hello, {name}!</div>;
};

export default Greeting;


# code 2


import React, { Component } from 'react';

interface CounterState {
  count: number; // 'count' should be a number
}

class Counter extends Component<{}, CounterState> {
  state: CounterState = {
    count: 0, // Initial value of count
  };

  increment = (): void => {
    this.setState({ count: this.state.count + 1 }); // Increase count by 1
  };

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}

export default Counter;
