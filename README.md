![55d54060803aad9797e8a9a4542d7c6](https://github.com/ruibabas/TJFstar/assets/116283117/6ceda94d-d34f-4178-abc1-47f6cdeed982)# TJFstar
say hello one

using UnityEngine;
 
public class Test : MonoBehaviour
{
    public float speed; //速度
    
    //判断手势
    private void JudgeGesture()
    {
        if (Input.touchCount == 1)
        {
            Touch touch = Input.GetTouch(0);
            if (touch.phase == TouchPhase.Moved)
            {
                Vector2 touchDeltaPosition = touch.deltaPosition;
                transform.Translate(touchDeltaPosition.x * speed, 0, 0);
            }
        }
    }
}
