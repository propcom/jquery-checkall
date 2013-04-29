# Check-all - a jQuery plugin

This is a simple jQuery plugin - like all the good ones - that associates
checkboxes with their 'check all' checkbox.

Simply select the 'check all' input and specify a selector or function for the
ones affected by it.

    $('.check-all').checkAll();

The plugin takes the `rel` attribute from the selected item. Alternatively you
may provide the `rel` option.

For styling purposes the check-all box is given a class 'checked' or
'part-checked' or neither. Since 'part-checked' is not an HTML concept the
class is provided for you; and for consistency the 'checked' class is also
provided.

An option `onChange` can be given a function to call whenever the state of the
check-all checkbox changes; from checked to unchecked or from either to
part-checked. Part-checked to part-checked is not considered a change, even if
the set of checked associated items changes.

    $('.check-all').checkAll({
		rel: '.checkme',
		onChange: function(elem) {
			if (elem.hasClass('part-checked')) {
				elem.parent().addClass('part-checked');
			}
			else {
				elem.parent().removeClass('part-checked');
			}
		}
	});

## Bugs

None known. Report [here](https://github.com/propcom/jquery-checkall/issues).
