If you specify both ``--nsExclude`` and ``--nsInclude``, the pattern 
that ``--nsExclude`` specifies takes precedence. For example, if you
specify both ``--nsExclude="prod.*"`` and ``--nsInclude="prod.trips"``, 
the pattern specified by ``--nsExclude`` takes precedence and no 
collections from the ``prod`` namespace are restored. 
