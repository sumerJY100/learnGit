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

