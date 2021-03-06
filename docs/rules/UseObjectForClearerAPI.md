# UseObjectForClearerAPI
**Category:** `pmd`<br/>
**Rule Key:** `pmd:UseObjectForClearerAPI`<br/>
> :warning: This rule is **deprecated** in favour of [S107](https://rules.sonarsource.com/java/RSPEC-107).

-----

When you write a public method, you should be thinking in terms of an API. If your method is public, it means other class
will use it, therefore, you want (or need) to offer a comprehensive and evolutive API. If you pass a lot of information
as a simple series of Strings, you may think of using an Object to represent all those information. You'll get a simplier
API (such as doWork(Workload workload), rather than a tedious series of Strings) and more importantly, if you need at some
point to pass extra data, you'll be able to do so by simply modifying or extending Workload without any modification to
your API. Example:
<pre>
public class MyClass {
  public void connect(String username,
    String pssd,
    String databaseName,
    String databaseAdress)
    // Instead of those parameters object
    // would ensure a cleaner API and permit
    // to add extra data transparently (no code change):
    // void connect(UserData data);
    {

  }
}
</pre>
