String locationStr1 = "A";
String locationStr2 = "��";
String rapperNumStr = "\\��վ��\"+locationStr1+"��"+locationStr2+"�ҵ�ǰ���������1";
long  rapperNum = getRealDBForInt(rapperNumStr);
String rapperStateStr = "\\��վ��\"+locationStr1+"��"+locationStr2+"�ҵ�ǰ�����״̬1";
long rapperState = getRealDBForInt(rapperStateStr);
String rapperTimeStr =  "\\��վ��\"+locationStr1 + locationStr2+"��������ʱ��";
long rapperTime  = HTConvertTime(\\��վ��\$��,\\��վ��\$��,\\��վ��\$��,\\��վ��\$ʱ,\\��վ��\$�� ,\\��վ��\$��);
setRealDBForInt(rapperTimeStr,rapperTime);
trace("rapperTimeStr:%s",rapperTimeStr);
long  i=16;
    
    
	String targetAddress = "\\��վ��\"+locationStr1 + locationStr2+"�����Y"  + strFromInt(i,10);

    	String target_alarmStr1 = "\\��վ��\"+locationStr1 + locationStr2+"�����·Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\��վ��\"+locationStr1 + locationStr2+"������·Y" + strFromInt(i,10);
 //   bool runState = getRealDBForBool(targetAddress);
 //   	bool alarmState1 = getRealDBForBool(target_alarmStr1);
 //   	bool alarmState2 = getRealDBForBool(target_alarmStr2);



while(i<182){
	String targetAddress = "\\��վ��\"+locationStr1 + locationStr2+"�����Y"  + strFromInt(i,10);
    if(rapperNum  == i){
    	String target_alarmStr1 = "\\��վ��\"+locationStr1 + locationStr2+"�����·Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\��վ��\"+locationStr1 + locationStr2+"������·Y" + strFromInt(i,10);
    bool runState = getRealDBForBool(targetAddress);
    	bool alarmState1 = getRealDBForBool(target_alarmStr1);
    	bool alarmState2 = getRealDBForBool(target_alarmStr2);

        //�������
        if(rapperState == 1){
            if(runState == 0){
                SetRealDBForInt(targetAddress ,1);
            }
            //����ϴ��Ǹ澯״̬����澯״̬��λ

             if(alarmState1 == 1){
            	SetRealDBForBool(target_alarmStr1,0);
            }
             if(alarmState2 == 1){
            	SetRealDBForBool(target_alarmStr2,0);
            }

       }else{

//��·�澯
            if(rapperState == 2){
	       		if(alarmState1 == 0){
	            	SetRealDBForBool(target_alarmStr1,1);
	           }
			}else{
				if(alarmState1 == 1){
	            	SetRealDBForBool(target_alarmStr1,0);
	            }
	       }
			//��·�澯
			if(rapperState == 3){
				if(alarmState2 == 0){
			    	SetRealDBForBool(target_alarmStr2,1);
			    }
			}else{
				if(alarmState2 == 1){
			    	SetRealDBForBool(target_alarmStr2,0);
			    }
			}
		}
	}else{
           if(runState == 1){
  		    SetRealDBForInt(targetAddress ,0);
           }
	}
    i = i + 1;    
}

