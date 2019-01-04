* 要aria-label标签来为辅助设备提供相应的标识
* 为了避免屏幕识读设备抓取非故意的和可能产生混淆的输出内容（尤其是当图标纯粹作为装饰用途时），我们为这些图标设置了 aria-hidden=“true” 属性
* html 里面的 role 本质上是增强语义性，当现有的HTML标签不能充分表达语义性的时候，就可以借助role来说明。通常这种情况出现在一些自定义的组件上，这样可增强组件的可访问性、可用性和可交互性.role是无障碍阅读，是给有阅读障碍的人设置的属性，有阅读障碍的人可以用读屏软件来解析，跟正常人没多大关系。可以不设置，不设置的话读屏软件就无法解析，有阅读障碍的人也就"看"不了了
* aria-current: page,  indicate that it represents the current page.

## aria-pressed
aria-pressed: Defines the button as a toggle button. The value of aria-pressed describes the state of the button. 
  * aria-pressed="false" when a button is not currently pressed
  *  aria-pressed="true" to indicate a button is currently pressed
  *  aria-pressed="mixed" if the button is considered to be partially pressed. 
  *  If the attribute is omitted or set to its default value of aria-pressed="undefined", the element does not support being pressed

## aria-disabled
Disabled buttons should include the `aria-disabled="true"` attribute to indicate the state of the element to assistive technologies

```HTML
// bootstrap example
<a href="#" class="... disabled" tabindex="-1" role="button" aria-disabled="true">Primary link</a>

```