# webdev-hw01
def convert(ident):
    """Converts cell identifier to col, row form"""
    i, col, row = 0, "", ""
    while i < len(ident) and ident[i].isalpha():
        col += ident[i]
        i += 1
    while i < len(ident) and ident[i].isdecimal():
        row += ident[i]
        i += 1
    if i != len(ident) or col == "" or row == "" or row[0] == 0:
        return None, None
    return col.upper(), row
