# ConvertThis
C# extension methods to help converting between types.

Can handle most common objects.

For example:

DataRow dr = GetDataRow();
int i = dr.Column<int>("CellName");

Or:

object obj = GetObject();
int i = obj.ToInt(-1);

Or:

CheckBox cb = GetCheckBox();
bool isChecked = cb.ToBool();

Decimals can be converted to Integer types and you can specify how rounding is handled:

object obj = "1.5";
int i = obj.ToInt(0, Rounding.Up);

NOTES:
The current version uses objects and reflection. This can be slow if iterating lots of objects.

