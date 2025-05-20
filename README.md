# ArrayList in C language
A shared library which provides a set of functions for handling ArrayList in C language. ArrayList is a flexible data container which allows user to store multiple datatypes in the same sequence and also offers fixed time access to individual elements in any order.


<h2>How to download?</h2>
You can download it <a href="https://github.com/user-attachments/files/20354307/libArrayList.zip">here</a>

<h2>How to install?</h2>
Unzip the downloaded file and move libArrayList.so to /usr/lib

<h2>How to link?</h2>
You can link the library to your C project as follows: gcc example.c -l ArrayList

<br>
<h2> Examples </h2>

* Example A:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "ArrayList.h"

int main()
{
    ArrayList *values = ArrayList_object();

    ArrayList_IL a[] = {$L(char('A')), $L("ABC"), $L(100)};

    for (size_t i = 0; i < 3; i++)
    {
        ArrayList_push(values, a[i]);
    }

    ArrayList_IL_destructor(a, 3);
    
    ArrayList_println(values);

    ArrayList_delete(values);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> ['A', "ABC", 100] </pre>

* Example A:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "ArrayList.h"

int main()
{
    ArrayList* data = ArrayList_object();
    
    ArrayList_push(data, "Hello world");
    ArrayList_push(data, (char)'Z');
    ArrayList_push(data, 123);
    ArrayList_push(data, 0.123);
    
    ArrayList_println(data);

    ArrayList_delete(data);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> ["Hello world", 'Z', 123, 0.123] </pre>
