## Halcon支持的颜色及其名称，共21种
[Halcon支持的颜色及其名称，共21种](https://blog.csdn.net/bitezijie/article/details/8858541)
[Halcon编程的语句颜色区分](https://blog.csdn.net/bitezijie/article/details/8858389)

*  在set_color的算子中，列出Halcon支持的颜色代码，共21种。   
*  Suggested values: 'black', 'white', 'red', 'green',   
*  'blue', 'cyan', 'magenta', 'yellow', 'dim gray', 'gray',   
*  'light gray', 'medium slate blue', 'coral', 'slate blue',   
*  'spring green', 'orange red', 'orange', 'dark olive green',   
*  'pink', 'forest green','cadet blue'   
*  可以用以下的代码来测试颜色   
ColorSet:=[]   
ColorSet[1]:='gray'   
ColorSet[2]:='magenta'   
ColorSet[3]:='dim gray'   
ColorSet[4]:='coral'   
ColorSet[5]:='slate blue'   
ColorSet[6]:='spring green'   
ColorSet[7]:='orange red'   
ColorSet[8]:='cadet blue'   
ColorSet[9]:='light gray'   
ColorSet[10]:='medium slate blue'   
ColorSet[11]:='red'   
ColorSet[12]:='white'   
ColorSet[13]:='green'   
ColorSet[14]:='blue'   
ColorSet[15]:='yellow'   
ColorSet[16]:='pink'   
ColorSet[17]:='orange'   
ColorSet[18]:='cyan'   
ColorSet[19]:='black'   
ColorSet[20]:='dark olive green'   
ColorSet[21]:='forest green'   
  
for i:=1 to 21 by 1   
    dev_update_window('off')   
    dev_close_window()   
    dev_open_window(0,0,300,300,ColorSet[i],WindowHandle)   
    get_system ('operating_system', OS)   
    set_display_font (WindowHandle, 16, 'mono', 'true', 'false')   
    disp_message (WindowHandle, ['The Color is:',ColorSet[i], 'window', -1, -1, [ColorSet,ColorSet], 'true')   
    wait_seconds(1)     
endfor
