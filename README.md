# React-Native-ViewPager

## Usage

### Install from npm:
`npm install --save rn-viewpager`

### Integrate into your app:  

```  
import React, {Component, StyleSheet, View, Text} from 'react-native';
import {IndicatorViewPager, PagerTitleIndicator, PagerDotIndicator} from 'rn-viewpager';


export default class ViewPagerPage extends Component {
    state = {
        count: 0
    };

    render() {
        console.log('render:' + this.state.count);
        return (
            <View style={{flex:1}}>
                <IndicatorViewPager
                    style={{height:200}}
                    indicator={this._renderDotIndicator()}
                >
                    <View style={{backgroundColor:'cadetblue'}}>
                        <Text>{'count' + this.state.count}</Text>
                    </View>
                    <View style={{backgroundColor:'cornflowerblue'}}>
                        <Text>page two</Text>
                    </View>
                    <View style={{backgroundColor:'#1AA094'}}>
                        <Text>page three</Text>
                    </View>
                </IndicatorViewPager>

                <IndicatorViewPager
                    style={{flex:1,marginTop:10}}
                    indicator={this._renderTitleIndicator()}
                >
                    <View style={{backgroundColor:'cadetblue'}}>
                        <Text>{'count' + this.state.count}</Text>
                    </View>
                    <View style={{backgroundColor:'cornflowerblue'}}>
                        <Text>page two</Text>
                    </View>
                    <View style={{backgroundColor:'#1AA094'}}>
                        <Text>page three</Text>
                    </View>
                </IndicatorViewPager>
            </View>
        );
    }

    _renderTitleIndicator() {
        return (
            <PagerTitleIndicator
                titles={['one', 'two', 'three']}
            />
        );
    }

    _renderDotIndicator() {
        return (
            <PagerDotIndicator
                pageCount={3}
            />
        );
    }
}
```

## TODO