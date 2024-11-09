Checks for duplicate literal, constant, or variable elements in Set.

### Example:

    # bad
    Set[:foo, :bar, :foo]

    # good
    Set[:foo, :bar]

    # bad
    Set.new([:foo, :bar, :foo])

    # good
    Set.new([:foo, :bar])

    # bad
    [:foo, :bar, :foo].to_set

    # good
    [:foo, :bar].to_set
