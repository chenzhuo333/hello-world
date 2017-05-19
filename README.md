# hello-world
This is my first code 
import xml.etree.ElementTree as ET

tree = ET.ElementTree(file = "NewFile.xml")

root = tree.getroot()

#for child in root:
#    print child.tag,child.attrib
print root.tag

print root[0].tag
print root[1].tag
print root[0].attrib

print root[0][2].tag #最多就两个Index
print root[0][2].text


for els in tree.iter(tag='login'): #tree 对象有一个iter遍历函数， 制定某一个tag进行遍历操作,如果不制定tag，就会把所有元素遍历一遍
    print els.tag, els.attrib
