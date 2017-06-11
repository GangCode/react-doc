# React 生命周期

    import React,{Component} from 'react';

    export default class App extends Component {

        /**
            react初始化state和props
            ES6的constructor取代react的getInitialState()和getDefaultProps()
        **/
        constructor(props){
            super(props);
            this.state = {
                name : 'react',
                sum : 0
            };
            this.handleInputNumber = this.handleInputNumber.bind(this);
        }

        /**
            组件装载前调用
            可以更改初始state
        **/
        componentWillMount(){
            this.setState({
                name : 'angular'
            });
        }

        /**
            组件装载并渲染UI
        **/
        render(){
            let text = `${this.state.name} community!`;

            return(
                 <div>
                    <h1>Welcome to {text}</h1>
                    <h1>sum = {this.state.sum}</h1>
                    <input type="text" onChange={this.handleInputNumber} placeholder="请输入数值"/>
                 </div>
            );
        }

        handleInputNumber(e){
            let numVal = e.target.value;
            let sum = this.state.sum + numVal;
            this.setState({
                sum : sum
            });
        }

        /**
            组件装载完成
        **/
        componentDidMount(){

        }
    }

