# angular6_material_demo
非常干净的演示代码 Angular6 + Material

## 项目创建步骤
### 创建一个干净的初始项目

````
npm install @angular/cli
````
````
ng new angular6_material_demo --sass
````
````
cd angular6_material_demo
````
````
npm install
````

测试一下看看项目能不能跑通
````
ng serve --open 0  
````
### 添加Material模块
#### Step 1: Install Angular Material, Angular CDK and Angular Animations

````
npm install --save @angular/material @angular/cdk @angular/animations
````
####  Step 2: Configure animations
在 app.module.ts
````
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

@NgModule({
  ...
  imports: [BrowserAnimationsModule],
  ...
})
export class PizzaPartyAppModule { }
````
#### Step 3: Import the component modules
在 app.module.ts
````
import {MatButtonModule, MatCheckboxModule} from '@angular/material';

@NgModule({
  ...
  imports: [MatButtonModule, MatCheckboxModule],
  ...
})
export class PizzaPartyAppModule { }
````
#### Step 4: Include a theme
在style.css
````
@import "~@angular/material/prebuilt-themes/indigo-pink.css";
````
#### Step 5: Gesture Support
````
npm install --save hammerjs
````
#### Step 6 (Optional): Add Material Icons
在index.html
````
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
````
### 使用Schematics命令快速生成文件
#### 导航 Schematic
````
ng generate @angular/material:material-nav --name <component-name>
````
#### Dashboard Schematic
````
ng generate @angular/material:material-dashboard --name <component-name>
````
