# SuspiciousConstantFieldName
**Category:** `pmd`<br/>
**Rule Key:** `pmd:SuspiciousConstantFieldName`<br/>
> :warning: This rule is **deprecated** in favour of [S116](https://rules.sonarsource.com/java/RSPEC-116).

-----

A field name is all in uppercase characters, which in Sun's Java naming conventions indicate a constant. However, the field is not final. Example :
<pre>
public class Foo {
  // this is bad, since someone could accidentally
  // do PI = 2.71828; which is actualy e
  // final double PI = 3.16; is ok
  double PI = 3.16;
}
</pre>
