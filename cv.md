# Artem Kanashkov

### Contacts:
* __Telegram:__ @US3R88
* __Skype:__ skypevandal
* __Email:__ temavandal@gmail.com

### Summary:
I just want to make some __iOS__ magic

### Education:
* Baranovichi State University. Bachelor's degree. Information Systems and Technologies. _2011_
* Self-education (e.g. codecademy, udemy courses, etc)

### English:
__B1__. I have experience communicating with __English__-speaking partners. Mostly correspondence.

### Skills:
* Python
* XML, HTML, CSS
* GIT, SVN
* SQL

### Code example:
```python
def parpaint(file):
    global pa
    tree = ET.parse(file)
    root = tree.getroot()
    for member in root.findall('itemGroup'):
        for m in member.findall('paint'):
            try:
                idx = m.find('id').text
                txt = m.find('userString').text
                pr = str(txt[txt.find(":") + 1:])
                ws4.cell(row=pa, column=1).value = 'Paint'
                ws4.cell(row=pa, column=2).value = int(idx)
                ws4.cell(row=pa, column=3).value = parloc(pr[:-1], custom_loc)[7:]
                ws4.cell(row=pa, column=4).value = parloc(pr[:-1], en_text_path)[7:]
                try:
                    ws4.cell(row=pa, column=5).value = m.find('tags').text
                    if 'hidden' in m.find('tags').text:
                        ws4.cell(row=pa, column=5).fill = PatternFill(fill_type='solid', start_color='fce0e0')
                except AttributeError:
                    pass
                pa += 1
            except TypeError:
                print("! Something wrong with ", m.find('userString').text)
                ws4.cell(row=pa, column=3).value = m.find('userString').text
                pa += 1
```
