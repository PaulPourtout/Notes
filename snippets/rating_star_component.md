# Snippet for a rating star ui component

```javascript
import React from 'react'
import CN from 'classnames'

type Value = string

type Props = {
  value: Value[],
  id: string,
  name: string,
  onChange: (Value[]) => void,
}

const SCORE_VALUES = [1, 2, 3, 4, 5]

export default class ScoreSelectInput extends React.Component<Props> {
  constructor(props) {
    super(props)

    this.state = {
      hoveredValue: null,
    }
  }

  handleMouseOut() {
    this.setState({
      hoveredValue: null,
    })
  }


  handleMouseOver(x) {
    this.setState({
      hoveredValue: x,
    })
  }

  render() {
    const {id, name, value, onChange} = this.props
    const displayValue = this.state.hoveredValue || value

    return (
      <div id={id} name={name} className="scoreSelectInput">

        {SCORE_VALUES.map((x, i) => (
          <input
            key={i}
            type="radio"

            className={CN('radio-star', displayValue != null && x <= displayValue ? 'filled-radio-star' : '')}
            onClick={() => onChange(x)}
            onMouseOver={() => this.handleMouseOver(x)}
            onMouseOut={() => this.handleMouseOut()}
          />
        ))}
      </div>

    )
  }
}

```
