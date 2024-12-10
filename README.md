:running:BGABadgeView-Android桥接React Native案例:running:
============

[BGABadgeView-Android](https://github.com/bingoogolapple/BGABadgeView-Android)

### 效果图
![Image of RecyclerViewDemo](https://raw.githubusercontent.com/bingoogolapple/react-native-bga-badge-view/master/screenshots/demo1.gif)

```
import BGABadgeViewAndroid from './app/Components/BGABadge/BGABadgeViewAndroid';
import DemoItem from './app/Components/demo/DemoItem';

class BGABadgeViewRN extends Component {

  constructor(props) {
    super(props);
    this.state = {
      badgeText: "20",
    };
  }

  render() {
    return (
      <View style={styles.container}>
        <Text style={{paddingBottom: 30, fontSize: 22, color: '#50a3fc'}}>React Native - BGABadgeView</Text>

        <DemoItem title="显示第一个徽章" handleClick={this.showFistBadge.bind(this)} />
        <DemoItem title="隐藏第一个徽章" handleClick={this.hiddenFistBadge.bind(this)} />
        <BGABadgeViewAndroid dragable={false} textBadge={this.state.badgeText} style={styles.badge} onDismiss={() => this.onDismiss("第1个")} />

        <BGABadgeViewAndroid badgeBgColor="#00ff00" badgeTextColor="#ff0000" badgePaddingDp={10} badgeTextSizeSp={14} textBadge="9" style={styles.badge} onDismiss={() => this.onDismiss("第2个")} />

        <BGABadgeViewAndroid textBadge="99" style={styles.badge} onDismiss={() => this.onDismiss("第3个")} />

        <BGABadgeViewAndroid circlePointBadge={true} badgePaddingDp={6} style={styles.badge} onDismiss={() => this.onDismiss("第4个")} />

        <Image source={{uri: 'https://avatars2.githubusercontent.com/u/8949716'}}
       style={styles.backgroundImage} resizeMode={Image.resizeMode.contain} >
        <BGABadgeViewAndroid drawableBadge="avatar_vip" style={{
          width: 30,
          height: 20,
        }} onDismiss={() => this.onDismiss("第5个")} />
        </Image>
      </View>
    );
  }

  onDismiss(tip) {
    ToastAndroid.show('消失 ' + tip, ToastAndroid.SHORT)
  }

  hiddenFistBadge() {
    this.setState({
          badgeText: ""
        });
  }

  showFistBadge() {
    this.setState({
          badgeText: "20"
        });
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    flexDirection: 'column',
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  badge: {
    width: 60,
    height: 60,
  },
  backgroundImage: {
    flexDirection: 'row',
    justifyContent: 'flex-end',
    flex: 1,
    width: 100,
    height: 100,
  }
});
```

## 作者联系方式

| 个人主页 | 邮箱 |
| ------------- | ------------ |
| <a  href="https://www.bingoogolapple.cn" target="_blank">bingoogolapple.cn</a>  | <a href="mailto:bingoogolapple@gmail.com" target="_blank">bingoogolapple@gmail.com</a> |

| 个人微信号 | 微信群 | 公众号 |
| ------------ | ------------ | ------------ |
| <img width="180" alt="个人微信号" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/BGAQrCode.png"> | <img width="180" alt="微信群" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/WeChatGroup1QrCode.jpg"> | <img width="180" alt="公众号" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/GongZhongHao.png"> |

| 个人 QQ 号 | QQ 群 |
| ------------ | ------------ |
| <img width="180" alt="个人 QQ 号" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/BGAQQQrCode.jpg"> | <img width="180" alt="QQ 群" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/QQGroup1QrCode.jpg"> |

## 打赏支持作者

如果您觉得 BGA 系列开源库或工具软件帮您节省了大量的开发时间，可以扫描下方的二维码打赏支持。您的支持将鼓励我继续创作，打赏后还可以加我微信免费开通一年 [上帝小助手浏览器扩展/插件开发平台](https://github.com/bingoogolapple/bga-god-assistant-config) 的会员服务

| 微信 | QQ | 支付宝 |
| ------------- | ------------- | ------------- |
| <img width="180" alt="微信" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/donate-wechat.jpg"> | <img width="180" alt="QQ" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/donate-qq.jpg"> | <img width="180" alt="支付宝" src="https://github.com/bingoogolapple/bga-god-assistant-config/raw/main/images/donate-alipay.jpg"> |

## 作者项目推荐

* 欢迎您使用我开发的第一个独立开发软件产品 [上帝小助手浏览器扩展/插件开发平台](https://github.com/bingoogolapple/bga-god-assistant-config)

## License

    Copyright 2016 bingoogolapple

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
