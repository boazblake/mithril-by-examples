---
title: React Integration
date: 2021-10-26
tags: [react, lifecycle, dom, components]
level: expert
version: 2.0.4
author: barneycarroll
credits: []
links: []
layout: layouts/example.html
flems:
  files:
    - name: .js
      compiler: babel
  links:
    - react/umd/react.development.js
    - react-dom/umd/react-dom.development.js
---

Integrate react components into a mithrl app.

~~~js
class ReactComponent extends React.Component {
  constructor(){
    super()

    this.state = { count : 0 }
  }

  render(){
    return [
      <p key="0">
        Count: {this.state.count}
      </p>,

      <button key="1" onClick={() => {
        this.setState({count: this.state.count + 1})
      }}>
        Increment
      </button>
    ]
  }
}

const MithrilComponent = () => {
  let showSubComponent = false

  return {
    view: () => [
      m('label',
        m('input[type=checkbox]', {
          onchange: e => {
            showSubComponent = e.target.checked
          }
        }),

        'Render React component?'
      ),

      m('br'),

      showSubComponent &&
        m('.ReactBridge', {
          oncreate: v => {
            ReactDOM.render(<ReactComponent/>, v.dom)
          },
        })
    ]
  }
}

m.mount(document.body, MithrilComponent)
~~~