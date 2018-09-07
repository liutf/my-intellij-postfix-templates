# my-intellij-postfix-templates
Custom Postfix Templates for Intellij IDEA. 自定义postfix模板

> v2.x 版本

![](http://7viho5.com1.z0.glb.clouddn.com/20180907215017.png)





> v1.x 版本

* 添加内容，在`## IDEA development templates ##`前追加

```java

### liutf ###

.newi : new instance
	CLASS                    →  $expr$ $var:suggestVariableName()$ = new $expr$();

.equals : StringUtils equals
	java.lang.String     	 →  if (StringUtils.equals("$END$",$expr$)){\
	                                                         \
	                                                       }

.notEmpty : CollectionUtils isNotEmpty
	java.util.Collection     →  if (CollectionUtils.isNotEmpty($expr$)){\
	                                                         $END$\
	                                                       }

.isEmpty : CollectionUtils isEmpty
	java.util.Collection     →  if (CollectionUtils.isEmpty($expr$)){\
	                                                         $END$\
	                                                       }

.isNotBlank : StringUtils isNotBlank
	java.lang.String     	 →  if (StringUtils.isNotBlank($expr$)){\
	                                                         $END$\
	                                                       }
.isBlank : StringUtils isBlank
	java.lang.String     	 →  if (StringUtils.isBlank($expr$)){\
	                                                         $END$\
	                                                       }

.isNumeric : StringUtils isNumeric
	java.lang.String     	 →  if (StringUtils.isNumeric($expr$)){\
	                                                         $END$\
	                                                       }

.checkNotBlank : Precondition checkArgumentNotBlank
	java.lang.String     	 →  Precondition.checkIsNotBlank("$expr$",$expr$);

.checkNotNull : Preconditions.checkNotNull
	java.lang.Object     	 →  Preconditions.checkNotNull($expr$);$END$

```
