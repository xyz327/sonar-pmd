# CommentDefaultAccessModifier
**Category:** `pmd`<br/>
**Rule Key:** `pmd:CommentDefaultAccessModifier`<br/>


-----

<p>
  To avoid mistakes if we want that a Method, Field or Nested class have a default access modifier
  we must add a comment at the beginning of the Method, Field or Nested class.
  By default the comment must be /* default */, if you want another, you have to provide a regex.
</p>

<pre>
public class Foo {
    final String stringValue = "some string";
    String getString() {
       return stringValue;
    }

    class NestedFoo {
    }
}

// should be
public class Foo {
  /* default */ final String stringValue = "some string";
  /* default */ String getString() {
     return stringValue;
  }

  /* default */ class NestedFoo {
  }
}
</pre>
