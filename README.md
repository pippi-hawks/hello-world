# hello-world

class HelloMessage extends React.Component {
  render() {
    return (
      <div>
        Hi {this.props.name}
      </div>
    );
  }
}

ReactDOM.render(
  <HelloMessage name="Pippi" />,
  mountNode
);

class Timer extends React.Component {
  constructor(props) {
    super(props);
    this.state = { seconds: 0 };
  }

  tick() {
    this.setState(prevState => ({
      seconds: prevState.seconds + 1
    }));
  }

  componentDidMount() {
    this.interval = setInterval(() => this.tick(), 1000);
  }
