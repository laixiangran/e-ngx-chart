# essence-ng2-chart

essence-ng2-chart is an Angular directive that can draw a chart.

## Usage

1. Install

	```shell
	npm install --save essence-ng2-chart
	```

2. Add the EssenceNg2PrintModule

	```typescript
	import {EssenceNg2ChartModule} from "essence-ng2-chart";
	@NgModule({
	    imports: [
	        EssenceNg2ChartModule
	    ]
	})
	```

3. template

	```html
	<div class="chart-main" essence-ng2-chart [chart]="chart"></div>
	```

4. component

	```typescript
	import {EssenceChart} from "essence-ng2-chart";
	
	chart = new EssenceChart({
    		chart: {
    			type: "column"
    		},
    		title: {
    			text: ""
    		},
    		xAxis: {
    			categories: ["西冉村", "宝山", "苗寨", "四季青", "北坞村", "金河闸", "田村", "香山"],
    			title: {
    				text: null
    			},
    			tickLength: 0
    		},
    		yAxis: {
    			min: 0,
    			title: {
    				text: null
    			},
    			labels: {
    				align: "center"
    			}
    		},
    		series: [{
    			data: [100, 120, 130, 140, 250, 160, 230, 180]
    		}],
    		credits: {
    			enabled: false
    		},
    		legend: {
    			enabled: false
    		},
    		tooltip: {
    			enabled: false
    		}
    	});
	```

## API

### Inputs

- `chart`（`EssenceChart`） - new EssenceChart(options)时，options与[Highcharts的配置属性](https://api.hcharts.cn/highcharts)一致

### Outputs

- `ready` - 初始化完成的事件，$event为当前EssenceNg2ChartDirective实例

### Instance Method

- `destroy` - 销毁图表控件

# License

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](/LICENSE)