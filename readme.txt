String locationStr1 = "A";
String locationStr2 = "左";
String rapperNumStr = "\\本站点\"+locationStr1+"列"+locationStr2+"室当前振打器锤号1";
long  rapperNum = getRealDBForInt(rapperNumStr);
String rapperStateStr = "\\本站点\"+locationStr1+"列"+locationStr2+"室当前振打器状态1";
long rapperState = getRealDBForInt(rapperStateStr);
String rapperTimeStr =  "\\本站点\"+locationStr1 + locationStr2+"侧振打锤振打时间";
long rapperTime  = HTConvertTime(\\本站点\$年,\\本站点\$月,\\本站点\$日,\\本站点\$时,\\本站点\$分 ,\\本站点\$秒);
setRealDBForInt(rapperTimeStr,rapperTime);
trace("rapperTimeStr:%s",rapperTimeStr);
long  i=16;
    
    
	       }
			//开路告警
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

