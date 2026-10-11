# Xbox-controller-part-1
using UnityEngine;

public class XboxControllerTest : MonoBehaviour
{
    void Update()
    {
        // 1. Sol Analog Çubuk Hareketleri
        float moveX = Input.GetAxis("Horizontal"); // A/D veya Sol Analog X ekseni
        float moveY = Input.GetAxis("Vertical");   // W/S veya Sol Analog Y ekseni

        if (Mathf.Abs(moveX) > 0.1f || Mathf.Abs(moveY) > 0.1f)
        {
            Debug.Log($"Sol Analog -> X: {moveX:F2}, Y: {moveY:F2}");
        }

        // 2. Buton Kontrolleri (Xbox Kolu Tuşları)
        // Button 0: A Tuşu | Button 1: B Tuşu | Button 2: X Tuşu | Button 3: Y Tuşu
        if (Input.GetKeyDown(KeyCode.Joystick1Button0))
        {
            Debug.Log("A butonuna basıldı!");
        }

        if (Input.GetKeyDown(KeyCode.Joystick1Button1))
        {
            Debug.Log("B butonuna basıldı!");
        }

        // 3. Omuz Tuşları ve Tetikler (LB / RB / LT / RT)
        if (Input.GetKeyDown(KeyCode.Joystick1Button4))
        {
            Debug.Log("LB (Sol Omuz) tuşuna basıldı!");
        }
        
        if (Input.GetKeyDown(KeyCode.Joystick1Button5))
        {
            Debug.Log("RB (Sağ Omuz) tuşuna basıldı!");
        }
    }
}
