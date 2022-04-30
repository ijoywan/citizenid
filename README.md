检验一个身份证号码的格式是否正确，并且可以获取到生日，性别，办证区域

P.S. 此包来自 `cszchen\citizenid` 因为那个包都不在了，所以只能自己传一个

安装
===

`composer require ijoywan/citizenid`

使用
===

```php
use ijoywan\citizenid;
    
$parser = new Parser();
$parser->setId($id);
    
//身份证号码格式是否正确
$parser->isValidate();
    
//获取生日，格式YYYYmmdd
$parser->getBirthday();
    
//获取性别, 1-男， 0-女，对应的常量为Parser::GENDER_MALE, Parser::FEMALE
$parser->getGender()
    
//获取行政区域,返回数组包含省，市，县，完整区域
$parser->getRegion();
```	
