***********************************************
Vim-YAPIF (Yet Another Python Indentation File)
***********************************************

This is yet another Python indentation file for Vim. It is largely based
off of `a script by Eric McSween
<http://www.vim.org/scripts/script.php?script_id=974>`_ and `a revised
script by Zhu Nianyang
<http://www.vim.org/scripts/script.php?script_id=3461>`_.

This style prefers to align the opening and closing
parentheses/braces/brackets on the same column when continuing long
lines like so::

    l_one = [1, 2, 3
             4, 5
            ]


    def func_with_arguments_long_lines(arg1, arg2, arg3, arg4,
                                       arg5, arg6
                                      ):
        pass


    myobj.a_cool_method_call(arg1, arg2, arg3, arg4,
                             arg5, arg6
                            )

In this manner, the indentation follows the `Google Python Style Guide
<http://google-styleguide.googlecode.com/svn/trunk/pyguide.html>`_.

For lists, tuples, dictionaries (and assignments to these structures) as
well as function or method calls, when parentheses/braces/brackets
appear at the end of a line alone, this style will indent the closing
parenthesis/brace/bracket at the same level::

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

    def func_with_arguments_separate_lines(
            arg1,
            arg2,
            arg3,
            arg4,
            arg5,
            arg6
        ):
        pass


    myobj.a_cooler_method_call(
        arg1,
        arg2,
        arg3,
        arg4,
        arg5,
        arg6
    )


A major difference between this indentation style and the two previous
styles is in the definition of functions and methods, where if the
opening parenthesis ends the first line, all the parameter lines are
indented by *two* levels past the opening line, while the closing
parenthesis is indented only one level past the opening line::

    def func_with_arguments_separate_lines(
            arg1,
            arg2,
            arg3,
            arg4,
            arg5,
            arg6
        ):
        pass

