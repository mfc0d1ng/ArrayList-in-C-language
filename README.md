# ArrayList in C language
A shared library which provides a set of functions for handling ArrayList in C language. ArrayList is a flexible data container which allows user to store multiple datatypes in the same sequence and also offers fixed time access to individual elements in any order.


<h2>How to download?</h2>
You can download it <a href="https://github.com/user-attachments/files/20266766/libArrayList.zip">here</a>

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

#define $(__x)  ArrayList_make(__x)

int main()
{
    ArrayList* data = ArrayList_object();
    
    ArrayList_data* elements[] = {$((char)'A'), $("ABC"), $(10), $(0.12)};

    for (size_t i = 0; i < 4; i++)
    {
        ArrayList_push(data, elements[i]);
    }
    
    printf("ArrayList data: ");
    ArrayList_display(data);

    ArrayList_delete(data);
    return EXIT_SUCCESS;
}
</code>
</pre>
