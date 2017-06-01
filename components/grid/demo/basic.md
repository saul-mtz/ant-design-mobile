---
order: 0
title:
  zh-CN: 基本
  en-US: Basic
---

````jsx
import { Grid, Tabs } from 'antd-mobile';

const data = Array.from(new Array(9)).map((_val, i) => ({
  icon: 'https://os.alipayobjects.com/rmsportal/IptWdCkrtkAUfjE.png',
  text: `name${i}`,
}));

const data1 = Array.from(new Array(2)).map((_val, i) => ({
  img: 'https://zos.alipayobjects.com/rmsportal/wIjMDnsrDoPPcIV.png',
  text: `name${i}`,
}));

const GridExample = () => (
  <div>

    <Tabs>
      <Tabs.TabPane key="1" tab="1">
          <Grid data={data1} columnNum={3} isCarousel onClick={(_el, index) => alert(index)} />
      </Tabs.TabPane>
      <Tabs.TabPane key="2" tab="2">
          <Grid data={data} columnNum={3} isCarousel onClick={(_el, index) => alert(index)} />
      </Tabs.TabPane>
    </Tabs>


  </div>
);

ReactDOM.render(<GridExample />, mountNode);
````

````css
.am-grid {
  border: 1px solid #ddd;
}
.sub-title {
  color: #888;
  font-size: .28rem;
  padding: 30px 0 18px 0;
}
````
