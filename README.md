using Battle.DiceAttackEffect;
using LOR_DiceSystem;
using LOR_XML;
using Mod;
using Sound;
using System;
using System.Collections.Generic;
using Battle.CreatureEffect;
using System.IO;
using System.Reflection;
using System.Xml.Serialization;
using TMPro;
using UI;
using UnityEngine;
using UnityEngine.UI;

public class BehaviourAction_blackswordX : BehaviourActionBase
{
    // Token: 0x06001122 RID: 4386 RVA: 0x0008A9B4 File Offset: 0x00088BB4
    public override List<RencounterManager.MovingAction> GetMovingAction(ref RencounterManager.ActionAfterBehaviour self, ref RencounterManager.ActionAfterBehaviour opponent)
    {
        bool flag = false;
        if (opponent.behaviourResultData != null)
        {
            flag = opponent.behaviourResultData.IsFarAtk();
        }
        if (self.result == Result.Win)
        {
            List<RencounterManager.MovingAction> list = new List<RencounterManager.MovingAction>();
            RencounterManager.MovingAction movingAction = new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.MoveForward, 30f, false, 0.001f, 1f);
            movingAction.customEffectRes = "FX_PC_RolRang_XSlash_Main";
            movingAction.SetEffectTiming(EffectTiming.PRE, EffectTiming.PRE, EffectTiming.PRE);
            new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.Stop, 0f, true, 0.1f, 1f).SetEffectTiming(EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT);
            list.Add(movingAction);
            opponent.infoList.Add(new RencounterManager.MovingAction(ActionDetail.Damaged, CharMoveState.Stop, 1f, false, 0.5f, 1f));
            return list;
        }
        return base.GetMovingAction(ref self, ref opponent);
    }
}

public class BehaviourAction_green1 : BehaviourActionBase
{
    // Token: 0x06001122 RID: 4386 RVA: 0x0008A9B4 File Offset: 0x00088BB4
    public override List<RencounterManager.MovingAction> GetMovingAction(ref RencounterManager.ActionAfterBehaviour self, ref RencounterManager.ActionAfterBehaviour opponent)
    {
        bool flag = false;
        if (opponent.behaviourResultData != null)
        {
            flag = opponent.behaviourResultData.IsFarAtk();
        }
        if (self.result == Result.Win)
        {
            List<RencounterManager.MovingAction> list = new List<RencounterManager.MovingAction>();
            RencounterManager.MovingAction movingAction = new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.MoveForward, 30f, false, 0f, 1f);
            movingAction.customEffectRes = "FX_IllusionCard_1_M_FairyTrail1";
            movingAction.SetEffectTiming(EffectTiming.PRE, EffectTiming.PRE, EffectTiming.PRE);
            new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.Stop, 0f, true, 0.1f, 1f).SetEffectTiming(EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT);
            list.Add(movingAction);
            opponent.infoList.Add(new RencounterManager.MovingAction(ActionDetail.Damaged, CharMoveState.Stop, 1f, false, 0.01f, 1f));
            return list;
        }
        return base.GetMovingAction(ref self, ref opponent);
    }
}

public class BehaviourAction_green2 : BehaviourActionBase
{
    // Token: 0x06001122 RID: 4386 RVA: 0x0008A9B4 File Offset: 0x00088BB4
    public override List<RencounterManager.MovingAction> GetMovingAction(ref RencounterManager.ActionAfterBehaviour self, ref RencounterManager.ActionAfterBehaviour opponent)
    {
        bool flag = false;
        if (opponent.behaviourResultData != null)
        {
            flag = opponent.behaviourResultData.IsFarAtk();
        }
        if (self.result == Result.Win)
        {
            List<RencounterManager.MovingAction> list = new List<RencounterManager.MovingAction>();
            RencounterManager.MovingAction movingAction = new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.MoveForward, 30f, false, 0f, 1f);
            movingAction.customEffectRes = "FX_IllusionCard_1_M_FairyTrail2";
            movingAction.SetEffectTiming(EffectTiming.PRE, EffectTiming.PRE, EffectTiming.PRE);
            new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.Stop, 0f, true, 0.1f, 1f).SetEffectTiming(EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT);
            list.Add(movingAction);
            opponent.infoList.Add(new RencounterManager.MovingAction(ActionDetail.Damaged, CharMoveState.Stop, 1f, false, 0.01f, 1f));
            return list;
        }
        return base.GetMovingAction(ref self, ref opponent);
    }
}
public class BehaviourAction_whiteswordGreat : BehaviourActionBase
{
    // Token: 0x06001122 RID: 4386 RVA: 0x0008A9B4 File Offset: 0x00088BB4
    public override List<RencounterManager.MovingAction> GetMovingAction(ref RencounterManager.ActionAfterBehaviour self, ref RencounterManager.ActionAfterBehaviour opponent)
    {
        bool flag = false;
        if (opponent.behaviourResultData != null)
        {
            flag = opponent.behaviourResultData.IsFarAtk();
        }
        if (self.result == Result.Win)
        {
            List<RencounterManager.MovingAction> list = new List<RencounterManager.MovingAction>();
            RencounterManager.MovingAction movingAction = new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.MoveForward, 30f, false, 0.001f, 1f);
            movingAction.customEffectRes = "AngelicaGreatSword_S1";
            movingAction.SetEffectTiming(EffectTiming.PRE, EffectTiming.PRE, EffectTiming.PRE);
            new RencounterManager.MovingAction(ActionDetail.Slash, CharMoveState.Stop, 0f, true, 0.1f, 1f).SetEffectTiming(EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT, EffectTiming.NOT_PRINT);
            list.Add(movingAction);
            opponent.infoList.Add(new RencounterManager.MovingAction(ActionDetail.Damaged, CharMoveState.Stop, 1f, false, 0.5f, 1f));
            return list;
        }
        return base.GetMovingAction(ref self, ref opponent);
    }
}

public class BehaviourAction_greensword : BehaviourActionBase
{
    // Token: 0x0600496C RID: 18796 RVA: 0x00193EF8 File Offset: 0x001920F8
    public override List<RencounterManager.MovingAction> GetMovingAction(ref RencounterManager.ActionAfterBehaviour self, ref RencounterManager.ActionAfterBehaviour opponent)
    {
        bool flag = false;
        if (opponent.behaviourResultData != null)
        {
            flag = opponent.behaviourResultData.IsFarAtk();
        }
        List<RencounterManager.MovingAction> list = new List<RencounterManager.MovingAction>();
        if (self.result == Result.Win)
        {
            self.preventOverlap = false;
            ActionDetail actionDetail = ActionDetail.S3;
            string customEffectRes = "FX_IllusionCard_1_M_FairyTrail1";
            if (BehaviourAction_greensword._motionCount++ % 2 == 1)
            {
                actionDetail = ActionDetail.S4;
                customEffectRes = "FX_IllusionCard_1_M_FairyTrail2";
            }
            self.behaviourResultData.diceBehaviourResult.actionDetail = actionDetail;
            RencounterManager.MovingAction movingAction = new RencounterManager.MovingAction(actionDetail, CharMoveState.TeleportBack, 1f, false, 0.02f, 1f);
            movingAction.customEffectRes = customEffectRes;
            movingAction.dstRotation = 30f;
            movingAction.dstDistance = 4f;
            movingAction.SetEffectTiming(EffectTiming.PRE, EffectTiming.PRE, EffectTiming.PRE);
            list.Add(movingAction);
            opponent.infoList.Add(new RencounterManager.MovingAction(ActionDetail.Damaged, CharMoveState.Stop, 1f, false, 0f, 1f));
        }
        else
        {
            list = base.GetMovingAction(ref self, ref opponent);
        }
        return list;
    }

    // Token: 0x0600496D RID: 18797 RVA: 0x00005931 File Offset: 0x00003B31
    public override bool IsMovable()
    {
        return false;
    }

    // Token: 0x04003585 RID: 13701
    private static int _motionCount;
}

public class BehaviourAction_white2 : BehaviourActionBase
{
    // Token: 0x0600496C RID: 18796 RVA: 0x00193EF8 File Offset: 0x001920F8
    public override List<RencounterManager.MovingAction> GetMovingAction(ref RencounterManager.ActionAfterBehaviour self, ref RencounterManager.ActionAfterBehaviour opponent)
    {
        bool flag = false;
        if (opponent.behaviourResultData != null)
        {
            flag = opponent.behaviourResultData.IsFarAtk();
        }
        List<RencounterManager.MovingAction> list = new List<RencounterManager.MovingAction>();
        if (self.result == Result.Win)
        {
            self.preventOverlap = false;
            ActionDetail actionDetail = ActionDetail.S3;
            string customEffectRes = "AngelicaLance_Z";
            if (BehaviourAction_white2._motionCount++ % 2 == 1)
            {
                actionDetail = ActionDetail.S4;
                customEffectRes = "AngelicaGreatSword_S1";
            }
            self.behaviourResultData.diceBehaviourResult.actionDetail = actionDetail;
            RencounterManager.MovingAction movingAction = new RencounterManager.MovingAction(actionDetail, CharMoveState.TeleportBack, 1f, false, 0.02f, 1f);
            movingAction.customEffectRes = customEffectRes;
            movingAction.dstRotation = 30f;
            movingAction.dstDistance = 4f;
            movingAction.SetEffectTiming(EffectTiming.PRE, EffectTiming.PRE, EffectTiming.PRE);
            list.Add(movingAction);
            opponent.infoList.Add(new RencounterManager.MovingAction(ActionDetail.Damaged, CharMoveState.Stop, 1f, false, 0f, 1f));
        }
        else
        {
            list = base.GetMovingAction(ref self, ref opponent);
        }
        return list;
    }

    public override bool IsMovable()
    {
        return false;
    }
    private static int _motionCount;
}
 
