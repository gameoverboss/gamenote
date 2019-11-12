#showtooltip 缴械
/startattack
/cast 防御姿态
/cast 缴械

#showtooltip 嘲讽
/startattack
/cast 防御姿态
/cast 嘲讽

压制/复仇/旋风斩
#showtooltip
/startattack
/cast [stance:1]压制;/cast [stance:2]复仇;/cast [stance:3]旋风斩

#showtooltip
/startattack
/cast [stance:1]斩杀;/cast [stance:2]嘲讽;/cast [stance:3]斩杀

远程开怪
#showtooltip
/startattack
/cast 枪械射击
/cast 弩射击
/cast 弓射击
/cast 投掷

#show [stance:1]冲锋; [stance:3]拦截
/dismount [mounted]
/startattack
/cast [nocombat,stance:1] 冲锋; [nocombat,nostance:1] 战斗姿态; [combat,nostance:3] 狂暴姿态; [combat,stance:3] 拦截


#showtooltip
/startattack
/cancelaura 剑刃风暴 
/cancelaura 保护之手 
/cast [help]援护;冲锋
/cast 英勇投掷
/cast 断筋


#showtooltip
/stopmacro [nocombat] 
/cast 鲁莽
/cast 天神下凡
/use 13
/use 14


#showtooltip 盾牌猛击
/startattack 
/console Sound_EnableSFX 0 
/castsequence reset=0.5 1,2,毁灭打击
/castsequence reset=0.5 1,复仇
/castsequence reset=0.5 盾牌猛击
/script UIErrorsFrame:Clear() 
/console Sound_EnableSFX 1


# show 狂暴之怒
/cast [nostance:3]狂暴姿态;狂暴之怒
/cast [nostance:2]防御姿态


冲锋/援护/拦截
#showtooltip
/dismount [exists]
/cast [stance:2,targefocus,exists][stance:2,harm,targetargettarget][stance:2,help][stance:2] 援护; [combat,nostance:3] 狂暴姿态; [stance:3] 拦截; 冲锋


移除拯救祝福
#showtooltip
/cancelaura [stance:2] 拯救祝福
/cast 血性狂暴


#showtooltip Last Stand
/cast 破釜沉舟
/bwcb 20 破釜沉舟


#showtooltip Shield Wall
/cast 盾墙
/bwcb 10 盾墙


盾牌猛击+毁灭
/castsequence [equipped:Shield] rese2 盾牌猛击, 毁灭, 毁灭
/cast [noequipped:Shield] 毁灭


格挡+复仇
/cast [equipped:Shield] 盾牌格挡
/cast 复仇
/cancelaura 拯救祝福
/cancelaura 强效拯救祝福


/cast [nocombat, stance:1]冲锋;[combat]乘胜追击


压制+英勇
/cast 压制
/cast 英勇打击


冲锋+拦截
#showtooltip
/cast [nocombat, stance:1]冲锋;[nocombat, nostance:1]战斗姿态;[combat, stance:3]拦截;[combat]狂暴姿态


打断
#showtooltip
/cast [stance:1/stance:3,equipped:盾牌]盾击;[stance:2]拳击



