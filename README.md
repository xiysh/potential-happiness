    asklist = []
    answerlist = []
    with open('D:\桌面\自然语言处理\医疗对话系统\Data_数据\IM_内科\内科5000-33000.csv') as f:
    for i in range(0,5000):
        lin = f.readline()[0:-1].split(',')
        if i==0:
            continue        
        print(lin)
        if len(lin) == 4:
            if len(lin[1]+','+lin[2])<200 and len(lin[3])<200:
                asklist.append(lin[1]+','+lin[2])
                answerlist.append(lin[3])
    with open('D:\桌面\自然语言处理\医疗对话系统\Data_数据\IM_内科\内科.txt','w') as f:
    for i in range(len(asklist)):
        f.write(asklist[i]+'\n'+answerlist[i]+'\n\n\n')
    
