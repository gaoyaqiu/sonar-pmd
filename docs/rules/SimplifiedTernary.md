# SimplifiedTernary
**Category:** `pmd`<br/>
**Rule Key:** `pmd:SimplifiedTernary`<br/>


-----

<p>
  Look for ternary operators with the form condition ? literalBoolean : foo or condition ? foo : literalBoolean.
</p>

<p>Examples:</p>
<pre>
public class Foo {
  public boolean test() {
    return condition ? true : something(); // can be as simple as return condition || something();
  }

  public void test2() {
    final boolean value = condition ? false : something(); // can be as simple as value = !condition && something();
  }

  public boolean test3() {
    return condition ? something() : true; // can be as simple as return !condition || something();
  }

  public void test4() {
    final boolean otherValue = condition ? something() : false; // can be as simple as condition && something();
  }
}
</pre>
