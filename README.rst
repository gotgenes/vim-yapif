***********************************************
Vim-YAPIF (Yet Another Python Indentation File)
***********************************************

This is yet another Python indentation file for Vim. It is largely based
off of `a script by Eric McSween
<http://www.vim.org/scripts/script.php?script_id=974>`_ and `a revised
script by Zhu Nianyang
<http://www.vim.org/scripts/script.php?script_id=3461>`_.

When continuing long lines, this style prefers to align the opening and
closing parentheses/braces/brackets on the same column like so::

    l_one = [1, 2, 3
             4, 5
            ]


    def func_with_arguments_long_lines(arg1, arg2, arg3, arg4,
                                       arg5, arg6
                                      ):
        pass


    myobj.a_method_call(arg1, arg2, arg3, arg4,
                        arg5, arg6
                       ):
        pass


In this manner, the indentation follows the `Google Python Style Guide
<http://google-styleguide.googlecode.com/svn/trunk/pyguide.html>`_.

For lists, tuples, dictionaries (and assignments to these structures),
when parentheses/braces/brackets appear at the end of a line alone, this
style will indent the closing parenthesis/brace/bracket at the same
level as the opening line::

    l_two = [
        1,
        2,
        3,
        4,
        5
    ]

    nested = {
        'a': (
            1,
            2
        ),
        'b': (
            3,
            4
        )
    }


Funcion and method calls similarly have a single level of indentation
for the lines between the enclosing parentheses::

    myobj.another_method_call(
        arg1,
        arg2,
        arg3,
        arg4,
        arg5,
        arg6
    )

    result = myfunc(
        'ham',
        'spam',
        'eggs'
    )


Statements ending with a ``:`` (colon) have two levels of indentation
for lines between the enclosing parentheses. This includes function,
method, and class declarations, if statements, and loops::

    class MyObj(
            MySuperClass1,
            MySuperClass2
        ):

        def func_with_arguments_separate_lines(
                arg1,
                arg2,
                arg3,
                arg4,
                arg5,
                arg6
            ):

            if (
                    condition1 and
                    condition2 and not
                    condition3
                ):
                while (
                        True is True and
                        False is False
                    ):
                    for x in (
                            1,
                            2,
                            3
                        ):
                        pass

