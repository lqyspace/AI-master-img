[toc]

> **final与static**

```java
public final class SaturnSystemErrorGroup {

	public static final int SUCCESS = 200;

	// general fail
	public static final int FAIL = 500;

	public static final int TIMEOUT = 550;

	// alarm will be raised with this error code
	public static final int FAIL_NEED_RAISE_ALARM = 551;

	public static Set<Integer> getAllSystemErrorGroups(){
		Set<Integer> resultSet = new HashSet<>();
		resultSet.add(SUCCESS);
		resultSet.add(FAIL);
		resultSet.add(TIMEOUT);
		resultSet.add(FAIL_NEED_RAISE_ALARM);

		return resultSet;
	}

}
```

**static**

- 加载：statis在类加载时初始化（加载）完成。
- 含义：static意为静态的，但凡被static修饰说明其是属于类的，但是是不属于类的对象的。
- 可修饰：static可修饰 `内部类`、`方法`、`成员变量`、`代码块`。
- 不可修饰：static不可修饰 `外部类`、`局部变量`【static是属于类的、局部变量是属于其方法的，并不属于类】
- 注意，`static`关键字不可兼容`this`关键字【static代表类层次，this代表当前类的对象】
- 构造方法不是静态方法，构造方法可以有this
- 

