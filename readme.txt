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
    
    
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);

    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
 //   bool runState = getRealDBForBool(targetAddress);
 //   	bool alarmState1 = getRealDBForBool(target_alarmStr1);
 //   	bool alarmState2 = getRealDBForBool(target_alarmStr2);



while(i<182){
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);
    if(rapperNum  == i){
    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
    bool runState = getRealDBForBool(targetAddress);
    	bool alarmState1 = getRealDBForBool(target_alarmStr1);
    	bool alarmState2 = getRealDBForBool(target_alarmStr2);

        //振打正常
        if(rapperState == 1){
            if(runState == 0){
                SetRealDBForInt(targetAddress ,1);
            }
            //如果上次是告警状态，则告警状态复位

             if(alarmState1 == 1){
            	SetRealDBForBool(target_alarmStr1,0);
            }
             if(alarmState2 == 1){
            	SetRealDBForBool(target_alarmStr2,0);
            }

       }else{

//短路告警
            if(rapperState == 2){
	       		if(alarmState1 == 0){
	            	SetRealDBForBool(target_alarmStr1,1);
	           }
			}else{
				if(alarmState1 == 1){
	            	SetRealDBForBool(target_alarmStr1,0);
	            }
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
    
    
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);

    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
 //   bool runState = getRealDBForBool(targetAddress);
 //   	bool alarmState1 = getRealDBForBool(target_alarmStr1);
 //   	bool alarmState2 = getRealDBForBool(target_alarmStr2);



while(i<182){
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);
    if(rapperNum  == i){
    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
    bool runState = getRealDBForBool(targetAddress);
    	bool alarmState1 = getRealDBForBool(target_alarmStr1);
    	bool alarmState2 = getRealDBForBool(target_alarmStr2);

        //振打正常
        if(rapperState == 1){
            if(runState == 0){
                SetRealDBForInt(targetAddress ,1);
            }
            //如果上次是告警状态，则告警状态复位

             if(alarmState1 == 1){
            	SetRealDBForBool(target_alarmStr1,0);
            }
             if(alarmState2 == 1){
            	SetRealDBForBool(target_alarmStr2,0);
            }

       }else{

//短路告警
            if(rapperState == 2){
	       		if(alarmState1 == 0){
	            	SetRealDBForBool(target_alarmStr1,1);
	           }
			}else{
				if(alarmState1 == 1){
	            	SetRealDBForBool(target_alarmStr1,0);
	            }
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
    
    
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);

    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
 //   bool runState = getRealDBForBool(targetAddress);
 //   	bool alarmState1 = getRealDBForBool(target_alarmStr1);
 //   	bool alarmState2 = getRealDBForBool(target_alarmStr2);



while(i<182){
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);
    if(rapperNum  == i){
    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
    bool runState = getRealDBForBool(targetAddress);
    	bool alarmState1 = getRealDBForBool(target_alarmStr1);
    	bool alarmState2 = getRealDBForBool(target_alarmStr2);

        //振打正常
        if(rapperState == 1){
            if(runState == 0){
                SetRealDBForInt(targetAddress ,1);
            }
            //如果上次是告警状态，则告警状态复位

             if(alarmState1 == 1){
            	SetRealDBForBool(target_alarmStr1,0);
            }
             if(alarmState2 == 1){
            	SetRealDBForBool(target_alarmStr2,0);
            }

       }else{

//短路告警
            if(rapperState == 2){
	       		if(alarmState1 == 0){
	            	SetRealDBForBool(target_alarmStr1,1);
	           }
			}else{
				if(alarmState1 == 1){
	            	SetRealDBForBool(target_alarmStr1,0);
	            }
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
    
    
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);

    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
 //   bool runState = getRealDBForBool(targetAddress);
 //   	bool alarmState1 = getRealDBForBool(target_alarmStr1);
 //   	bool alarmState2 = getRealDBForBool(target_alarmStr2);



while(i<182){
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);
    if(rapperNum  == i){
    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
    bool runState = getRealDBForBool(targetAddress);
    	bool alarmState1 = getRealDBForBool(target_alarmStr1);
    	bool alarmState2 = getRealDBForBool(target_alarmStr2);

        //振打正常
        if(rapperState == 1){
            if(runState == 0){
                SetRealDBForInt(targetAddress ,1);
            }
            //如果上次是告警状态，则告警状态复位

             if(alarmState1 == 1){
            	SetRealDBForBool(target_alarmStr1,0);
            }
             if(alarmState2 == 1){
            	SetRealDBForBool(target_alarmStr2,0);
            }

       }else{

//短路告警
            if(rapperState == 2){
	       		if(alarmState1 == 0){
	            	SetRealDBForBool(target_alarmStr1,1);
	           }
			}else{
				if(alarmState1 == 1){
	            	SetRealDBForBool(target_alarmStr1,0);
	            }
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
    
    
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);

    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
 //   bool runState = getRealDBForBool(targetAddress);
 //   	bool alarmState1 = getRealDBForBool(target_alarmStr1);
 //   	bool alarmState2 = getRealDBForBool(target_alarmStr2);



while(i<182){
	String targetAddress = "\\本站点\"+locationStr1 + locationStr2+"侧振打Y"  + strFromInt(i,10);
    if(rapperNum  == i){
    	String target_alarmStr1 = "\\本站点\"+locationStr1 + locationStr2+"侧振打开路Y" + strFromInt(i,10);
    	String target_alarmStr2 = "\\本站点\"+locationStr1 + locationStr2+"侧振打短路Y" + strFromInt(i,10);
    bool runState = getRealDBForBool(targetAddress);
    	bool alarmState1 = getRealDBForBool(target_alarmStr1);
    	bool alarmState2 = getRealDBForBool(target_alarmStr2);

        //振打正常
        if(rapperState == 1){
            if(runState == 0){
                SetRealDBForInt(targetAddress ,1);
            }
            //如果上次是告警状态，则告警状态复位

             if(alarmState1 == 1){
            	SetRealDBForBool(target_alarmStr1,0);
            }
             if(alarmState2 == 1){
            	SetRealDBForBool(target_alarmStr2,0);
            }

       }else{

//短路告警
            if(rapperState == 2){
	       		if(alarmState1 == 0){
	            	SetRealDBForBool(target_alarmStr1,1);
	           }
			}else{
				if(alarmState1 == 1){
	            	SetRealDBForBool(target_alarmStr1,0);
	            }
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

