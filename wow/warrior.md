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


防恐
# show 狂暴之怒
/cast [nostance:3]狂暴姿态;狂暴之怒
/cast [nostance:2]防御姿态


打断
#showtooltip [equipped:Shields,nostance:3]盾击; 拳击
#showtooltip [equipped:shield,nostance:3]盾击; 拳击
/stopcasting
/cast [nostance:3,noequipped:Shields] 狂暴姿态; [nostance:3,equipped:Shields]盾击; 拳击


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


盾牌猛击+2次毁灭
/castsequence [equipped:Shield] rese2 盾牌猛击, 毁灭, 毁灭
/cast [noequipped:Shield] 毁灭


格挡+复仇
/cast [equipped:Shield] 盾牌格挡
/cast 复仇
/cancelaura 拯救祝福
/cancelaura 强效拯救祝福


/cast [nocombat, stance:1]冲锋;[combat]乘胜追击


斩杀+嗜血
/castsequence reset=1 斩杀,嗜血


压制+英勇
/cast 压制
/cast 英勇打击


非战斗状态下，非战斗姿态则切换战斗姿态，战斗姿态则施放冲锋；战斗状态下，非狂暴姿态则切换狂暴姿态，狂暴姿态则施放拦截
#showtooltip
/cast [nocombat, stance:1]冲锋;[nocombat, nostance:1]战斗姿态;[combat, stance:3]拦截;[combat]狂暴姿态


战斗或防御姿态下，且装备了盾牌则施放盾击；狂暴姿态下施放拳击
#showtooltip
/cast [stance:1/stance:3,equipped:盾牌]盾击;[stance:2]拳击


#show [stance:1]冲锋; [stance:3]拦截
/dismount [mounted]
/startattack
/cast 断筋
/stopcasting
/cast [nocombat,stance:1] 冲锋; [nocombat,nostance:1] 战斗姿态;[combat,stance:3] 拦截


