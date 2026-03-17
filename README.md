# (o) MON 2 : SOUNDSCAPE MACHINE 🎛️
*Comprehensive User Manual & Documentation - Firmware Version 2.2*

----

## 📑 TABLE OF CONTENTS
1. **English Documentation**
2. **คู่มือภาษาไทย (Thai Documentation)**
3. **中文说明书 (Chinese Documentation)**
4. **Manual en Español (Spanish Documentation)**

<br><br><br>

---

# 1. 🇬🇧 English Documentation

## 1.1 Introduction and Safety Information
Welcome to the **MON 2 : Soundscape Machine**, a hardware synthesizer developed by Monkhum Craft and Creative (Chiang Mai). It is designed to be a limitless sonic playground, blending analog-style rotary control with a high-performance digital processing system.

**Key Features:**
- **6 Oscillators** with waveform shaping and LFO routing.
- **Polyphonic sound system** for Chord mode.
- **Sampler system** supporting customizable 16-bit 48kHz .wav files.
- **Built-in Step Sequencer** for creating continuous rhythms.
- **USB MIDI I/O** support for incoming and outgoing signals.

**Operation Caution:**
- Please use a standard USB-C power source (5V 1A recommended).
- When connecting an audio signal via the 3.5mm Output, it is always recommended to start with the lowest volume to prevent damage to your studio monitors or headphones.

## 1.2 Device Components and Boot System
The MON 2 is designed to be used in conjunction with an OLED display for ease of adjustment.

**Front Panel Overview:**
- **OLED Screen:** For displaying parameters, waveforms, and various menus.
- **3 Main Knobs (Top Row):** Used for adjusting parameters (e.g., Cutoff, Resonance, Volume, etc.), whose functions change depending on the currently displayed screen.
- **Push and Navigation Buttons (Bottom Matrix):** Used for changing screens, activating functions, and triggering sounds.

**Boot Protection System (Boot Lock):**
When turning on the device in Firmware 2.2, the system will delay the operation of the knobs for 3 seconds.
- **Reason:** Since the knobs are analog devices, their positions before booting might not match the saved presets. This delay prevents parameters from changing unintentionally.
- **How it works:** During the first 3 seconds, the system will not respond to knob turns. Afterwards, the system unlocks, allowing the knobs to control parameters normally again.

## 1.3 Screen Control and Smart Knobs System
Menu selection on the MON 2 operates via the OLED screen, grouping functions into Pages.

**Smart Knob Status Symbols:**
At the bottom of the OLED screen, the operational status of the knobs is displayed as follows:
1. `[====]` **Locked:** The parameter is locked and cannot be adjusted, preventing accidental turning.
2. `[ .  ]` **Ready:** The knob's position matches the saved value. It can be turned to adjust values immediately.
3. `[    ]` **Inactive:** The knob is not connected to any parameter on this screen.
4. `[ C  ]` **Catch Mode:** Occurs when entering a new screen where the knob's position differs from the saved value. Turning the knob will have no effect until the user turns it to match the current saved position. Once matched, the symbol changes to `[ . ]`, and values can be adjusted normally.

## 1.4 Voice Mode (Main Synthesizer)
The main mode of the MON 2 for Subtractive Synthesizer functionality.

**Oscillators (OSC 1, 2, and 3)**
- **Frequency Control:** Adjust the root pitch of each OSC.
- **Waveform Selection:** Mix between Sine, Triangle, Sawtooth, and Square waves.
- **Volume Balancing:** Control the volume of each OSC before entering the Filter system.

**Envelopes (ADSR System)**
- **Attack:** The resistance or fade-in time of the sound when a button is pressed.
- **Release:** The length or fade-out time of the sound tail when a button is released.

## 1.5 Chord Mode (Polyphonic Chords)
A polyphonic chord generation mode, creating a group of chord sounds with a single button press.
- **Root Note:** Select the starting musical note.
- **Chord Type:** Select the desired chord structure, including `[ Maj, Maj7, Min, Min7, 7th, 9th, Maj9 ]`.

## 1.6 Sampler Mode and WAV File Usage
**Entering Sampler Mode:**
Press `SHIFT + CT` to activate Sampler mode (the Voice/Chord synthesizer system will be paused).

**Sampling Slots Groups:**
- **Group 1:** Controlled by buttons `A1` and `A2`
- **Group 2:** Controlled by buttons `B1` and `B2`
- **Group 3:** Controlled by buttons `C1` and `C2`

**Playback Control:**
- **Pitch Control:** Adjust the playback speed and pitch.
- **Play Modes:** Play through once (one shot), play only while pressed (on-off), loop continuously (loop), or play backward (reverse).
- **Start/End Points:** Define the audio start and end points.
- **Fade In/Out:** Adjust the smoothness of the audio start and stop (FW 2.1 and above).

**Uploading WAV Files to the Device:**
1. Connect the device to a computer via USB cable.
2. Visit the website [MON 2 WAV Convertor](https://monkhumcc.github.io/mon2-wav-convertor/).
3. Drag and drop the desired audio files onto the website.
4. The system will automatically convert the files (16-bit / 48kHz / Mono mixdown) and install them into the selected slots.

## 1.7 Step Sequencer and Drum Simulation
**Activating the Step Sequencer:**
Touch and hold the **AT button for up to 3 seconds**. The screen will emit a light signal indicating that the Step Sequencer mode has begun.

**Programming Steps:**
- The touch button panel will display an 8 or 16-step grid format.
- Touch a button to turn the sound on or off for that step.
- The `Tempo` screen controls the speed (BPM).

## 1.8 Modulation, LFOs, and Effects System
**LFOs (Low Frequency Oscillators):**
MON 2 supports 3 independent LFO sets (LFO 1, LFO 2, LFO 3).
- **Freq:** Adjust the speed of the frequency cycle.
- **Depth:** Define the intensity level of the effect on the target.
- **Dest:** Define where the LFO will act, such as Osc Pitch, Filter Cutoff, or Volume.

**Filter (VCF):**
Controls the frequency range of the sound.
- **Cutoff (LPF Limit):** Cuts off the highest frequencies allowed to pass.
- **Resonance (LPF Q Power):** Increases the volume of the frequency exactly at the Cutoff point.

**Global Effects:**
- **Distortion (Drive):** Increases the level of overdrive or harmonic grit of the sound.
- **Echo / Delay:** Defines the echo by adjusting Feedback and Time values to create sonic depth.

## 1.9 System Settings (MIDI Connection / Pattern Saving)

### Multi-Pattern Memory System (6 Slots)
Users can save all custom settings on the device into 6 memory slots.
- Go to the `System` page.
- Select a memory slot number (1 - 6) and choose the Save command.
- All Sampler sounds will store their variables independently in each preset slot upon recall.

### USB MIDI Setup Protocol
MON 2 supports Class-Compliant connections via USB-C. The system will recognize the device as `(o) Monkhum.cc MIDI`.
- **Receiving Signal (Incoming MIDI):**
  - If you want MON 2 to act as a Sound Module receiving commands from an external DAW or MIDI Keyboard, press `SHIFT + AT` to enter signal receiving mode. A red LED will light up.
  - Turn to the `M6/6` page and set the Channel number to match your system.
  - Press `SHIFT + REC` to cancel and return to the default mode. The system is ready to receive external commands.
- **Sending Signal (Outgoing MIDI):**
  - The Step Sequencer mode can output note codes to control external programs or musical instruments via the USB port.

## 1.10 Shortcut Keys Summary

**In Main Synth Mode and Chord Mode:**
- Hold `CLR + Button A1` : Go to the OSC Frequency page
- Hold `CLR + Button A2` : Go to the Waveform & Volume page
- Hold `CLR + Button B1` : Go to the Mod OSC1 & Mod OSC2 page
- Hold `CLR + Button B2` : Go to the Mod OSC3 & Envelope OSC1 page
- Hold `CLR + Button C1` : Go to the Envelope OSC2 & Envelope OSC3 page
- Hold `CLR + Button C2` : Go to the Distortion & Filter page

**In Sampler Mode (Opened with `SHIFT + CT`):**
- Hold `CLR + Button A1` : Go to Sampler Slot 1 settings
- Hold `CLR + Button A2` : Go to Sampler Slot 2 settings
- Hold `CLR + Button B1` : Go to Sampler Slot 3 settings
- Hold `CLR + Button B2` : Go to Sampler Slot 4 settings
- Hold `CLR + Button C1` : Go to Sampler Slot 5 settings
- Hold `CLR + Button C2` : Go to Sampler Slot 6 settings

## 1.11 Firmware Update Guide

**Prerequisites:**
1. It is recommended to use Google Chrome or Microsoft Edge browsers.
2. Use only data-grade USB-C cables (Data Cable).
3. If connecting to the computer for the first time, it may be necessary to install the device reader software (driver `CH9102F / CH34XSER`) beforehand.

**Software Update Steps:**
1. Completely close any plugin windows (Cura, Serial USB monitors, or Arduino IDE windows) on the computer to reduce "port occupied" issues.
2. **Firmly touch and hold the `B2` button on the MON 2 panel!**
3. While your finger is still touching B2, **push the Power switch to turn on the device**. The screen will remain completely dark — meaning it has successfully entered Bootloader Flash Mode waiting for data.
4. Visit the website `https://monkhumcc.github.io/mon2-flash-tool/`
5. Click the `Connect / Install` window (blue button).
6. Wait for the browser to pop up a window asking for the connection port (Select a Port) - here, choose the *USB-SERIAL* port.
7. Approve the data transfer. **Do not unplug or pull the cable under any circumstances.** Wait for the loading to reach 100%. The device will reboot itself and be ready for use.

<br><br><br>

---

# 2. 🇹🇭 คู่มือภาษาไทย (Thai Documentation)

## 2.1 บทนำและคำแนะนำด้านความปลอดภัย
ยินดีต้อนรับสู่ **MON 2 : Soundscape Machine** เครื่องสังเคราะห์เสียงฮาร์ดแวร์ที่พัฒนาโดย ม่อนคำ คราฟท์ แอนด์ ครีเอทีฟ (เชียงใหม่) ซึ่งออกแบบมาเพื่อการสร้างสรรค์เสียงอย่างอิสระ ผสานการควบคุมผ่านปุ่มหมุนแบบอนาล็อกเข้ากับระบบประมวลผลดิจิทัลประสิทธิภาพสูง

**คุณสมบัติหลัก:**
- **Oscillator 6 ตัว** พร้อมการปรับแต่งรูปแบบคลื่นเสียงและการกำหนดเส้นทาง LFO
- **ระบบเสียงโพลีโฟนิก** สำหรับโหมดคอร์ด
- **ระบบ Sampler** รองรับไฟล์เสียง .wav 16-bit 48kHz ที่ปรับแต่งได้
- **Step Sequencer ในตัว** สำหรับการสร้างจังหวะต่อเนื่อง
- **รองรับการเชื่อมต่อ USB MIDI** ขาเข้าและขาออก

**ข้อควรระวังในการใช้งาน:**
- โปรดใช้แหล่งจ่ายไฟ USB-C ที่ได้มาตรฐาน (แนะนำ 5V 1A)
- เมื่อเชื่อมต่อสายสัญญาญเสียงผ่านช่อง Output 3.5 มม. แนะนำให้เริ่มต้นด้วยระดับเสียงที่เบาที่สุดเสมอ เพื่อป้องกันความเสียหายต่อลำโพงมอนิเตอร์หรือหูฟัง

## 2.2 ส่วนประกอบของตัวเครื่องและระบบเปิดเครื่อง
ตัวเครื่อง MON 2 ได้รับการออกแบบให้ใช้งานร่วมกับหน้าจอแสดงผล OLED เพื่อความสะดวกในการปรับแต่ง

**ภาพรวมแผงควบคุมด้านหน้า:**
- **หน้าจอ OLED:** สำหรับแสดงค่าพารามิเตอร์ รูปแบบคลื่น และเมนูต่างๆ
- **ลูกบิดหลัก 3 ตัว (เรียงด้านบนหน้าจอ):** ใช้สำหรับปรับค่าพารามิเตอร์ต่างๆ (เช่น Cutoff, Resonance, ระดับเสียง ฯลฯ) โดยหน้าที่ของลูกบิดจะเปลี่ยนไปตามหน้าจอที่แสดงผลอยู่
- **ปุ่มกดและนำทาง (ชุดเมทริกซ์ด้านล่าง):** ใช้สำหรับเปลี่ยนหน้าจอ เปิดใช้งานฟังก์ชันต่างๆ และสั่งงานเสียง

**ระบบป้องกันเมื่อเปิดเครื่อง (Boot Lock):**
เมื่อเปิดเครื่องใน Firmware 2.2 ระบบจะทำการหน่วงเวลาการทำงานของลูกบิดเป็นเวลา 3 วินาที
- **เหตุผล:** เนื่องจากลูกบิดเป็นอุปกรณ์อนาล็อก ตำแหน่งก่อนเปิดเครื่องอาจไม่ตรงกับค่าพรีเซ็ต (Preset) ที่บันทึกไว้ การหน่วงเวลาช่วยป้องกันไม่ให้ค่าพารามิเตอร์เปลี่ยนไปโดยไม่ได้ตั้งใจ
- **วิธีการทำงาน:** ในช่วง 3 วินาทีแรก ระบบจะไม่ตอบสนองต่อการหมุนลูกบิด หลังจากนั้นระบบจะปลดล็อกให้ลูกบิดควบคุมพารามิเตอร์กลับมาใช้งานได้ตามปกติ

## 2.3 การควบคุมหน้าจอและระบบลูกบิดอัจฉริยะ (Smart Knobs)
การเลือกเมนูของ MON 2 จะทำงานผ่านหน้าจอ OLED ที่จัดกลุ่มฟังก์ชันเป็นหน้าต่างๆ (Pages)

**สัญลักษณ์สถานะของลูกบิด (Smart Knob Interface):**
ที่ด้านล่างของหน้าจอ OLED จะแสดงสถานะการทำงานของลูกบิด ดังนี้:
1. `[====]` **Locked (ล็อก):** พารามิเตอร์ถูกล็อกไว้ ไม่สามารถปรับค่าได้ เพื่อป้องกันการหมุนโดยไม่ตั้งใจ
2. `[ .  ]` **Ready (พร้อมใช้งาน):** ตำแหน่งลูกบิดตรงกับค่าที่บันทึกไว้ สามารถหมุนเพื่อปรับค่าได้ทันที
3. `[    ]` **Inactive (ไม่ทำงาน):** ลูกบิดไม่ได้เชื่อมต่อกับพารามิเตอร์ใดๆ ในหน้าจอนี้
4. `[ C  ]` **Catch Mode (โหมดดักจับค่า):** เกิดขึ้นเมื่อเข้าสู่หน้าจอใหม่ และตำแหน่งลูกบิดแตกต่างจากค่าที่บันทึกไว้ การหมุนลูกบิดจะยังไม่มีผลใดๆ จนกว่าผู้ใช้จะหมุนลูกบิดไปถึงตำแหน่งที่ตรงกับค่าปัจจุบัน เมื่อตำแหน่งตรงกัน ระบบจะเปลี่ยนสัญลักษณ์เป็น `[ . ]` และสามารถปรับค่าได้ตามปกติ

## 2.4 โหมด Voice (เครื่องสังเคราะห์เสียงหลัก)
โหมดหลักของ MON 2 สำหรับการสังเคราะห์เสียงแบบ Subtractive Synthesizer

**ออสซิลเลเตอร์ (OSC 1, 2 และ 3)**
- **Frequency Control (การปรับความถี่):** ปรับระดับเสียงคีย์หลักของแต่ละ OSC
- **Waveform Selection (การเลือกรูปแบบคลื่น):** สามารถเลือกปรับผสมระหว่างคลื่น Sine, Triangle, Sawtooth และ Square
- **Volume Balancing (การปรับระดับเสียง):** ควบคุมความดังของแต่ละ OSC ก่อนส่งเข้าสู่ระบบ Filter

**Envelopes (ระบบ ADSR)**
- **Attack:** ความต้านทานของการเกิดเสียงเมื่อกดปุ่ม
- **Release:** ความยาวของการปล่อยหางเสียงเมื่อปล่อยปุ่ม

## 2.5 โหมด Chord (เสียงคอร์ดโพลีโฟนิก)
โหมดสร้างเสียงคอร์ดแบบโพลีโฟนิก โดยการกดปุ่มเพียงปุ่มเดียวเพื่อสร้างกลุ่มเสียงคอร์ด
- **Root Note (คีย์พื้นฐาน):** เลือกตัวโน้ตเริ่มต้น
- **Chord Type (รูปแบบคอร์ด):** เลือกโครงสร้างคอร์ดที่ต้องการ ได้แก่ `[ Maj, Maj7, Min, Min7, 7th, 9th, Maj9 ]`

## 2.6 โหมด Sampler และการใช้งานไฟล์ WAV
**การเข้าสู่โหมด Sampler:**
กดปุ่ม `SHIFT + CT` เพื่อเปิดใช้งานโหมด Sampler (ระบบสังเคราะห์เสียง Voice/Chord จะปรับเป็นพักการทำงาน)

**กลุ่มช่องบันทึกเสียง (Sampling Slots):**
- **กลุ่มที่ 1:** ควบคุมด้วยปุ่ม `A1` และ `A2`
- **กลุ่มที่ 2:** ควบคุมด้วยปุ่ม `B1` และ `B2`
- **กลุ่มที่ 3:** ควบคุมด้วยปุ่ม `C1` และ `C2`

**การควบคุมการเล่น (Playback):**
- **Pitch Control:** ปรับความเร็วและระดับความสูงตํ่าของเสียง
- **Play Modes:** เล่นเสียงตั้งแต่ต้นจนจบหนึ่งครั้ง (one shot), เล่นเฉพาะเมื่อกดปุ่ม (on-off), เล่นวนซ้ำ (loop), เล่นถอยหลัง (reverse)
- **Start/End Points:** กำหนดจุดเริ่มต้นและจุดสิ้นสุดของเสียง
- **Fade In/Out:** ปรับความนุ่มนวลในการเริ่มและหยุดเสียง (เฉพาะ FW 2.1 ขี้นไป)

**การอัปโหลดไฟล์เสียง WAV ไปยังอุปกรณ์:**
1. เชื่อมต่ออุปกรณ์กับคอมพิวเตอร์ผ่านสาย USB
2. เข้าสู่เว็บไซต์ [MON 2 WAV Convertor](https://monkhumcc.github.io/mon2-wav-convertor/)
3. ลากและวางไฟล์เสียงที่ต้องการลงในเว็บไซต์
4. ระบบจะทำการแปลงไฟล์ (16-bit / 48kHz / Mono mixdown) และติดตั้งลงในช่องที่เลือกโดยอัตโนมัติ

## 2.7 โหมด Step Sequencer และจำลองจังหวะกลอง
**สั่งเปิด Step Sequencer:**
ให้แตะบน **ปุ่มกด AT ค้างเอาไว้จนถึง 3 วินาที** หน้าจอจะแสดงสัญญาณแสงให้รู้ว่าในจังหวะนี้โหมด Step Sequencer เริ่มขึ้นแล้ว

**การกำหนดรูปแบบจังหวะ (Programming Steps):**
- แผงปุ่มสัมผัสจะแสดงรูปแบบช่องจังหวะแบบ 8 หรือ 16 ก้าว
- สามารถสัมผัสปุ่มเพื่อเปิดหรือปิดเสียงสำหรับจังหวะนั้นๆ
- หน้าจอ `Tempo` สำหรับควบคุมความเร็ว (BPM)

## 2.8 ระบบ Modulation, LFO และเอฟเฟกต์
**LFOs (Low Frequency Oscillators):**
MON 2 รองรับ LFO อิสระจำนวน 3 ชุด (LFO 1, LFO 2, LFO 3)
- **Freq (ความเร็ว):** ปรับความเร็วในการวนรอบความถี่
- **Depth (ความลึก):** กำหนดระดับความเข้มของผลกระทบต่อเป้าหมาย
- **Dest (เป้าหมาย):** กำหนดตำแหน่งที่ LFO จะกระทำ เช่น Osc Pitch, Filter Cutoff หรือ Volume

**Filter (ตัวกรองสัญญาณ VCF):**
ควบคุมย่านความถี่ของเสียง
- **Cutoff (พารามิเตอร์จำกัด LPF):** ตัดย่านความถี่สูงสุดที่ยอมให้ผ่าน
- **Resonance (กำลัง LPF Q):** เพิ่มความดังของย่านความถี่ตรงตำแหน่ง Cutoff

**Global Effects (เอฟเฟกต์ภาพรวม):**
- **Distortion (ระดับความผิดเพี้ยน - Drive):** เพิ่มระดับความขุ่นหรือแตกพร่าของเสียง
- **Echo / Delay (การสะท้อน):** กำหนดเสียงสะท้อน โดยปรับค่า Feedback และ Time เพื่อสร้างมิติของเสียง

## 2.9 การตั้งค่าระบบ (การเชื่อมต่อ MIDI / การบันทึก Pattern)

### พื้นที่ระบบความจำ Multi-Pattern (6 ช่องเก็บ)
ผู้ใช้สามารถเก็บบันทึกการปรับตั้งค่าทุกอย่างบนเครื่องไว้ในหน่วยความจำจำนวน 6 ช่อง (Memory Slots)
- ไปที่หน้า `System`
- เลือกหมายเลขช่องเก็บ (1 - 6) และเลือกคำสั่ง Save
- เสียง Sampler ทั้งหมดจะถูกตั้งค่าตัวแปรแยกอิสระในแต่ละช่องพรีเซ็ตเมื่อทำการเรียกคืนค่า

### โปรโตคอลแผงวงจร USB MIDI (USB MIDI Setup)
MON 2 รองรับการเชื่อมต่อแบบ Class-Compliant ผ่านสาย USB-C ระบบจะรู้จักอุปกรณ์ในชื่อ `(o) Monkhum.cc MIDI`
- **กรณีรับสัญญาณ (Incoming MIDI):**
  - หากคุณต้องการให้ MON 2 ทำหน้าที่เป็น Sound Module สำหรับรับคำสั่งจาก DAW หรือ MIDI Keyboard ภายนอก ให้กด `SHIFT + AT` เพื่อเข้าสู่โหมดรับสัญญาณ โดยจะมี LED สีแดง สว่างขึ้น
  - หมุนไปที่หน้า `M6/6` และกำหนดหมายเลข Channel ให้ตรงกับระบบ
  - กดยกเลิกกลับมาที่โหมดตั้งต้นด้วย `SHIFT + REC` ระบบก็พร้อมรับคำสั่งจากภายนอก
- **กรณีขอเป็นตัวจ่ายสัญญาณ (Outgoing MIDI):**
  - โหมด Step Sequencer สามารถจ่ายรหัสตัวโน้ตออกมาควบคุมโปรแกรมหรือเครื่องดนตรีภายนอกผ่านพอร์ต USB ได้

## 2.10 สรุปปุ่มคีย์ลัดบนหน้าจอ (Shortcut Keys)

**ในโหมดซินธ์หลัก และ โหมดคอร์ดดนตรี:**
- กดค้าง `CLR + ปุ่ม A1` : ไปยังหน้า OSC Frequency
- กดค้าง `CLR + ปุ่ม A2` : ไปยังหน้า Waveform & Volume
- กดค้าง `CLR + ปุ่ม B1` : ไปยังหน้า Mod OSC1 & Mod OSC2
- กดค้าง `CLR + ปุ่ม B2` : ไปยังหน้า Mod OSC3 & Envelope OSC1
- กดค้าง `CLR + ปุ่ม C1` : ไปยังหน้า Envelope OSC2 & Envelope OSC3
- กดค้าง `CLR + ปุ่ม C2` : ไปยังหน้า Distortion & Filter

**ในโหมด Sampler (เปิดด้วย `SHIFT + CT`):**
- กดค้าง `CLR + ปุ่ม A1` : ไปยังการตั้งค่า Sampler สล็อต 1
- กดค้าง `CLR + ปุ่ม A2` : ไปยังการตั้งค่า Sampler สล็อต 2
- กดค้าง `CLR + ปุ่ม B1` : ไปยังการตั้งค่า Sampler สล็อต 3
- กดค้าง `CLR + ปุ่ม B2` : ไปยังการตั้งค่า Sampler สล็อต 4
- กดค้าง `CLR + ปุ่ม C1` : ไปยังการตั้งค่า Sampler สล็อต 5
- กดค้าง `CLR + ปุ่ม C2` : ไปยังการตั้งค่า Sampler สล็อต 6

## 2.11 คู่มือการอัปเดต Firmware

**ข้อกำหนดเบื้องต้น:**
1. แนะนำให้ใช้เบราว์เซอร์ Google Chrome หรือ Microsoft Edge
2. ใช้เกรดสายส่งข้อมูล USB-C (Data Cable) เท่านั้น
3. หากเชื่อมต่อเข้ากับคอมพิวเตอร์เป็นครั้งแรก อาจมีความจำเป็นต้องติดตั้งโปรแกรมอ่านอุปกรณ์ (ไดรเวอร์ `CH9102F / CH34XSER`) ให้เรียบร้อยเสียก่อน

**ขั้นตอนการอัปเดตซอฟต์แวร์:**
1. ปิดหน้าต่างปลั๊กอิน (Cura, Serial USB monitors หรือหน้าต่างโปรแกรม Arduino IDE) บนคอมพิวเตอร์ให้สนิทเพื่อลดอาการ "พอร์ตโดนแย่ง"
2. **เอาหน้าปัดสัมผัสไปแตะทับปุ่ม `B2` ที่เครื่อง MON 2 เอาไว้ค้างกดแน่นๆ!**
3. พร้อมกับนิ้วยังแตะ B2 ก็ให้ดันและ **สับสวิตช์ Power ติดเครื่องรัน** หน้าจอจะต้องมืดทึบๆ ต่อไป — แสดงว่าเข้าสู่ Bootloader Flash Mode เพื่อรอรับข้อมูล
4. ไปที่หน้าเว็บไซต์ `https://monkhumcc.github.io/mon2-flash-tool/` 
5. คลิกหน้าต่าง `Connect / Install` (ปุ่มสีฟ้า)
6. รอเบราว์เซอร์จะเด้งหน้าต่างขึ้นมา ขอรายชื่อช่องการเชื่อมต่อ (Select a Port) - ตรงนี้ให้เลือกช่อง *USB-SERIAL* 
7. อนุมัติการส่งข้อมูล **ห้ามถอดปลั๊กหรือดึงสายเด็ดขาด** โหลดไปให้ถึง 100% เครื่องจะรีบูตตัวเองและพร้อมเปิดใช้งาน

<br><br><br>

---

# 3. 🇨🇳 中文说明书 (Chinese Documentation)

## 3.1 简介与安全建议
欢迎使用 **MON 2 : Soundscape Machine**! 这是一个由 Monkhum Craft and Creative (泰国清迈) 开发的硬件合成器。它专为无限的声音创造而设计，将模拟风格的旋钮控制与高性能数字处理系统完美融合。

**主要功能:**
- **6 个振荡器**, 支持波形调整和 LFO 路由。
- **复音系统** 专为和弦模式设计。
- **采样器系统** 支持自定义 16-bit 48kHz .wav 文件。
- **内置步进音序器** 用于创建连续节奏。
- **USB MIDI I/O** 支持接收和发送信号。

**操作注意事项:**
- 请使用标准的 USB-C 电源 (推荐 5V 1A)。
- 通过 3.5mm 输出连接音频信号时，建议始终从最低音量开始，以防止损坏您的录音室监听音箱或耳机。

## 3.2 设备组件与启动系统
MON 2 设计为与 OLED 显示屏结合使用，以方便进行调整。

**前面板概述:**
- **OLED 屏幕:** 用于显示参数、波形和各种菜单。
- **3 个主旋钮 (顶排):** 用于调整参数 (例如 截止频率、共鸣、音量等)，其功能会根据当前显示的屏幕而改变。
- **触摸导航按钮 (底部矩阵):** 用于切换屏幕、激活功能和触发声音。

**开机保护系统 (Boot Lock):**
在固件 2.2 中打开设备时，系统会将旋钮的操作延迟 3 秒。
- **原因:** 由于旋钮是模拟设备，开机前的位置可能与保存的预设不匹配。此延迟可防止参数被意外更改。
- **工作原理:** 在最初的 3 秒内，系统将不会响应旋钮的转动。之后，系统解锁，允许旋钮恢复正常控制参数。

## 3.3 屏幕控制与智能旋钮系统
MON 2 上的菜单选择通过 OLED 屏幕进行，将功能分组为不同的页面 (Pages)。

**智能旋钮状态符号:**
在 OLED 屏幕底部，旋钮的操作状态显示如下:
1. `[====]` **锁定 (Locked):** 参数被锁定且无法调整，防止意外转动。
2. `[ .  ]` **就绪 (Ready):** 旋钮位置与保存的数值相符。可以立即转动以调整数值。
3. `[    ]` **无效 (Inactive):** 在此屏幕上旋钮未连接到任何参数。
4. `[ C  ]` **捕捉模式 (Catch Mode):** 当进入新屏幕且旋钮位置与保存的数值不同时发生。转动旋钮将没有任何效果，直到用户将其转动到与当前保存位置匹配为止。一旦匹配，符号将变为 `[ . ]`，即可正常调整数值。

## 3.4 声音模式 (主合成器)
MON 2 的主要模式，提供减法合成器功能。

**振荡器 (OSC 1, 2, 和 3)**
- **频率控制:** 调整每个 OSC 的根音高。
- **波形选择:** 在 正弦波、三角波、锯齿波和方波之间进行混合。
- **音量平衡:** 在进入滤波器系统之前控制每个 OSC 的音量。

**包络线 (ADSR 系统)**
- **起音 (Attack):** 按下按钮时声音淡入的时间或阻力。
- **释放 (Release):** 松开按钮时声音尾部淡出的长度或时间。

## 3.5 和弦模式 (复音和弦)
复音和弦生成模式，按单键即可创建一组和弦声音。
- **根音 (Root Note):** 选择起始音符。
- **和弦类型 (Chord Type):** 选择所需的和弦结构，包括 `[ Maj, Maj7, Min, Min7, 7th, 9th, Maj9 ]`。

## 3.6 采样器模式与 WAV 文件使用
**进入采样器模式:**
按下 `SHIFT + CT` 激活采样器模式 (声音/和弦合成器系统将暂停)。

**采样槽分组:**
- **第 1 组:** 由按钮 `A1` 和 `A2` 控制
- **第 2 组:** 由按钮 `B1` 和 `B2` 控制
- **第 3 组:** 由按钮 `C1` 和 `C2` 控制

**播放控制:**
- **音高控制:** 调整播放速度和音高。
- **播放模式:** 播放一次 (one shot)、仅在按下时播放 (on-off)、连续循环 (loop) 或倒放 (reverse)。
- **起点/终点:** 定义音频的起点和终点。
- **淡入/淡出:** 调整音频开始和停止的平滑度 (FW 2.1 及以上)。

**将 WAV 文件上传到设备:**
1. 通过 USB 线将设备连接到电脑。
2. 访问网站 [MON 2 WAV Convertor](https://monkhumcc.github.io/mon2-wav-convertor/)。
3. 将所需的音频文件拖放到网站上。
4. 系统将自动转换文件 (16-bit / 48kHz / Mono mixdown) 并将其安装到选定的槽位。

## 3.7 步进音序器与鼓机模拟
**激活步进音序器:**
长按 **AT 按钮最多 3 秒**。屏幕将发出光信号，指示步进音序器模式已开始。

**编程步骤 (Programming Steps):**
- 触摸按钮面板将显示 8 步或 16 步网格格式。
- 触摸按钮以打开或关闭该步的声音。
- `Tempo` 屏幕用于控制速度 (BPM)。

## 3.8 调制、LFOs 与效果系统
**LFOs (低频振荡器):**
MON 2 支持 3 个独立的 LFO 组 (LFO 1, LFO 2, LFO 3)。
- **频率 (Freq):** 调整频率循环的速度。
- **深度 (Depth):** 定义由于对目标的效应程度。
- **目标 (Dest):** 定义 LFO 将在何处起作用，例如 Osc Pitch、 Filter Cutoff 或 Volume。

**滤波器 (VCF):**
控制声音的频率范围。
- **截止频率 (Cutoff):** 切断允许通过的最高频率 (低通限制)。
- **共鸣 (Resonance):** 增加正好在截止点处的频率音量 (LPF Q Power)。

**全局效果:**
- **失真 (Distortion/Drive):** 增加声音的过载级别或谐波颗粒感。
- **回声/延迟 (Echo / Delay):** 通过调整 Feedback 和 Time 值来定义回声，以创建声音深度。

## 3.9 系统设置 (MIDI 连接 / 保存)

### 多重模式内存系统 (6 个槽位)
用户可以将设备上的所有自定义设置保存到 6 个内存槽中。
- 前往 `System` 页面。
- 选择内存槽号 (1 - 6) 并选择 Save 命令。
- 调用时，所有采样器声音将在每个预设槽中独立存储其变量。

### USB MIDI 设置协议
MON 2 支持通过 USB-C 的类兼容连接 (Class-Compliant)。系统将识别该设备为 `(o) Monkhum.cc MIDI`。
- **接收信号 (Incoming MIDI):**
  - 如果您希望 MON 2 作为声音模块接收来自外部 DAW 或 MIDI 键盘的命令，请按 `SHIFT + AT` 进入信号接收模式。红色 LED 将亮起。
  - 翻到 `M6/6` 页面并设置与您的系统匹配的通道号。
  - 按 `SHIFT + REC` 取消并返回默认模式。系统已准备好接收外部命令。
- **发送信号 (Outgoing MIDI):**
  - 步进音序器模式可以通过 USB 端口输出音符代码，以控制外部程序或乐器。

## 3.10 快捷键总结

**在主合成器模式和和弦模式下:**
- 按住 `CLR + 按钮 A1` : 前往 OSC Frequency 页面
- 按住 `CLR + 按钮 A2` : 前往 Waveform & Volume 页面
- 按住 `CLR + 按钮 B1` : 前往 Mod OSC1 & Mod OSC2 页面
- 按住 `CLR + 按钮 B2` : 前往 Mod OSC3 & Envelope OSC1 页面
- 按住 `CLR + 按钮 C1` : 前往 Envelope OSC2 & Envelope OSC3 页面
- 按住 `CLR + 按钮 C2` : 前往 Distortion & Filter 页面

**在采样器模式下 (用 `SHIFT + CT` 打开):**
- 按住 `CLR + 按钮 A1` : 前往 Sampler Slot 1 设置
- 按住 `CLR + 按钮 A2` : 前往 Sampler Slot 2 设置
- 按住 `CLR + 按钮 B1` : 前往 Sampler Slot 3 设置
- 按住 `CLR + 按钮 B2` : 前往 Sampler Slot 4 设置
- 按住 `CLR + 按钮 C1` : 前往 Sampler Slot 5 设置
- 按住 `CLR + 按钮 C2` : 前往 Sampler Slot 6 设置

## 3.11 固件更新指南

**基本要求:**
- 建议使用 Google Chrome 或 Microsoft Edge 浏览器。
- 仅使用数据级 USB-C 线 (Data Cable)。
- 如果是首次连接到电脑，可能需要预先安装设备驱动程序 (`CH9102F / CH34XSER`)。

**软件更新步骤:**
1. 完全关闭电脑上的任何插件窗口 (Cura、Serial USB monitors 或 Arduino IDE 窗口) 以减少“端口被占用”问题。
2. **用力按住 MON 2 面板上的 `B2` 按钮不放！**
3. 在手指仍按住 B2 的同时，**推开电源开关开启设备**。屏幕将保持全黑 — 这意味着它已成功进入 Bootloader Flash Mode，正在等待数据。
4. 访问网站 `https://monkhumcc.github.io/mon2-flash-tool/`
5. 点击 `Connect / Install` 窗口 (蓝色按钮)。
6. 等待浏览器弹出一个要求连接端口的窗口 (Select a Port) - 在此，选择 *USB-SERIAL* 端口。
7. 批准数据传输。**在任何情况下都不要拔掉插头或拉扯线缆。** 等待加载达到 100%。设备将自行重启并准备使用。

<br><br><br>

---

# 4. 🇪🇸 Manual en Español (Spanish Documentation)

## 4.1 Introducción y Consejos de Seguridad
¡Bienvenido al **MON 2 : Soundscape Machine**! Un sintetizador de hardware desarrollado por Monkhum Craft and Creative (Chiang Mai) que está diseñado para ser un campo de juego sonoro ilimitado, combinando el control giratorio analógico con un sistema de procesamiento digital de alto rendimiento.

**Características Principales:**
- **6 Osciladores** que incluyen moldeado de onda y enrutamiento LFO.
- **Sistema de sonido polifónico** para el modo de Acorde (Chord).
- **Sistema Sampler** compatible con archivos .wav de 16-bit 48kHz personalizables.
- **Secuenciador de Pasos incorporado** para crear ritmos continuos.
- **Soporte USB MIDI I/O** para señales entrantes y salientes.

**Precauciones de Operación:**
- Por favor, use una fuente de alimentación USB-C estándar (se recomienda 5V 1A).
- Al conectar una señal de audio por la Salida de 3.5mm, siempre se recomienda comenzar con el volumen más bajo para prevenir daños a sus monitores de estudio o auriculares.

## 4.2 Componentes del Dispositivo y Sistema de Arranque
El MON 2 está diseñado para ser usado en conjunto con una pantalla OLED para facilitar su ajuste.

**Visión General del Panel Frontal:**
- **Pantalla OLED:** Para mostrar parámetros, formas de onda y diferentes menús.
- **3 Perillas Principales (Fila Superior):** Usadas para ajustar parámetros (e.g. Cutoff, Resonance, Volumen, etc.), las funciones cambian dependiendo de la pantalla actual.
- **Botones de Presión y Navegación (Matriz Inferior):** Usados para cambiar pantallas, activar funciones y lanzar sonidos.

**Sistema de Protección de Arranque (Boot Lock):**
Al encender el dispositivo en el Firmware 2.2, el sistema retrasará el funcionamiento de las perillas por 3 segundos.
- **Razón:** Ya que las perillas son dispositivos analógicos, sus posiciones antes del arranque pueden no coincidir con los presets guardados. Este retraso previene que los parámetros cambien involuntariamente.
- **Cómo funciona:** Durante los primeros 3 segundos, el sistema no responderá a la rotación de las perillas. Después, el sistema se desbloquea, permitiendo que las perillas controlen los parámetros de forma normal nuevamente.

## 4.3 Control de Pantalla y Sistema Smart Knobs
La selección del menú en el MON 2 opera mediante la pantalla OLED, agrupando funciones en Páginas (Pages).

**Símbolos de Estado del Smart Knob:**
En la parte inferior de la pantalla OLED, el estado operacional de los mandos giratorios se muestra así:
1. `[====]` **Bloqueado (Locked):** El parámetro está bloqueado y no se puede ajustar, previniendo rotación accidental.
2. `[ .  ]` **Listo (Ready):** La posición de la perilla coincide con el valor guardado. Puede girarse para ajustar los valores de inmediato.
3. `[    ]` **Inactivo (Inactive):** La perilla no está conectada a ningún parámetro en esta pantalla.
4. `[ C  ]` **Modo de Captura (Catch Mode):** Ocurre al entrar en una nueva pantalla donde la posición de la perilla difiere del valor guardado. Girar la perilla no tendrá efecto hasta que el usuario la rote para igualar la posición guardada actual. Una vez igualada, el símbolo cambia a `[ . ]`, y los valores pueden ser ajustados de forma normal.

## 4.4 Modo Voice (Sintetizador Principal)
El modo principal del MON 2 para la función de Sintetizador Sustractivo.

**Osciladores (OSC 1, 2, y 3)**
- **Control de Frecuencia:** Ajuste el tono raíz de cada OSC.
- **Selección de Forma de Onda:** Mezcle entre ondas Senoidal, Triangular, de Sierra y Cuadrada.
- **Balance de Volumen:** Controle el volumen de cada OSC antes de entrar en el sistema Filtro.

**Envolventes (Sistema ADSR)**
- **Ataque (Attack):** La resistencia o tiempo de entrada (fade-in) del sonido cuando se presiona un botón.
- **Relajación (Release):** La longitud o tiempo de atenuación (fade-out) de la cola del sonido al soltar el botón.

## 4.5 Modo Chord (Acordes Polifónicos)
Un modo de generación de acordes polifónicos, creando un grupo de sonidos combinados con pulsar un solo botón.
- **Nota Raíz (Root Note):** Seleccione la nota musical inicial.
- **Tipo de Acorde (Chord Type):** Seleccione la estructura de acorde deseada, incluyendo `[ Maj, Maj7, Min, Min7, 7th, 9th, Maj9 ]`.

## 4.6 Modo Sampler y Uso de Archivos WAV
**Entrar al Modo Sampler:**
Presione `SHIFT + CT` para activar el modo Sampler (el sistema sintetizador Voice/Chord se pausará).

**Grupos de Ranuras (Slots) de Muestreo:**
- **Grupo 1:** Controlado por los botones `A1` y `A2`
- **Grupo 2:** Controlado por los botones `B1` y `B2`
- **Grupo 3:** Controlado por los botones `C1` y `C2`

**Control de Reproducción:**
- **Control de Tono (Pitch):** Ajuste la velocidad de reproducción y el tono.
- **Modos de Reproducción:** Reproducir una vez (one shot), reproducir sólo mientras se pulsa (on-off), bucle continuo (loop), o reproducir hacia atrás (reverse).
- **Puntos de Inicio/Fin:** Defina los puntos de inicio y finalización del audio.
- **Fundidos (Fade In/Out):** Ajuste la suavidad del inicio y final del audio (FW 2.1 y superior).

**Subir Archivos WAV al Dispositivo:**
1. Conecte el dispositivo a un ordenador por cable USB.
2. Visite la página web [MON 2 WAV Convertor](https://monkhumcc.github.io/mon2-wav-convertor/).
3. Arrastre y suelte los archivos de audio deseados en el sitio web.
4. El sistema convertirá los archivos automáticamente (16-bit / 48kHz / Mono mixdown) y los instalará en las ranuras seleccionadas.

## 4.7 Secuenciador de Pasos y Simulación de Batería
**Activar el Secuenciador de Pasos:**
Toque y mantenga pulsado **el botón AT por hasta 3 segundos**. La pantalla emitirá una señal de luz indicando que el modo Step Sequencer ha comenzado.

**Programación de Pasos:**
- El panel táctil de botones mostrará un formato de cuadrícula (grid) de 8 o 16 pasos.
- Toque un botón para activar o desactivar el sonido en ese paso.
- La pantalla `Tempo` controla la velocidad (BPM).

## 4.8 Sistema de Modulación, LFOs, y Efectos
**LFOs (Osciladores de Baja Frecuencia):**
El MON 2 soporta 3 conjuntos de LFO individuales (LFO 1, LFO 2, LFO 3).
- **Velocidad (Freq):** Ajusta la velocidad del ciclo de frecuencia.
- **Profundidad (Depth):** Define el nivel de intensidad del efecto sobre el destino.
- **Destino (Dest):** Define donde actuará el LFO, tal como Tono OSC (Pitch), Corte del Filtro (Cutoff), o Volumen.

**Filtro (VCF):**
Controla el rango de frecuencia del sonido.
- **Corte de Frecuencia (Cutoff):** Corta las frecuencias más altas para no dejarlas pasar (Límite LPF).
- **Resonancia (Resonance):** Incrementa el volumen de la frecuencia exactamente en el punto de Corte (Poder LPF Q).

**Efectos Globales:**
- **Distorsión (Drive):** Incrementa el nivel de saturación o granularidad armónica del sonido.
- **Eco / Retardo (Delay):** Define el eco ajustando los valores de Realimentación (Feedback) y Tiempo para crear profundidad sonora.

## 4.9 Ajustes de Sistema (Conexión MIDI / Guardar Patrón)

### Sistema de Memoria Multi-Patrones (6 Slots)
Los usuarios pueden guardar todos los ajustes personalizados del dispositivo en 6 ranuras de memoria.
- Vaya a la página `System`.
- Seleccione el número en la ranura de memoria (1 - 6) y elija el comando Save (Guardar).
- Todos los sonidos del Sampler almacenarán sus variables de manera independiente en cada preset hasta ser recuperados.

### Protocolo de Configuración USB MIDI
MON 2 soporta conexiones Class-Compliant a través de USB-C. El sistema reconocerá el dispositivo como `(o) Monkhum.cc MIDI`.
- **Recepción de Señal (Incoming MIDI):**
  - Si desea que el MON 2 actúe como un Módulo de Sonido recibiendo comandos desde un DAW externo o Teclado MIDI, presione `SHIFT + AT` para entrar al modo de recepción de señal. Un LED rojo se encenderá.
  - Vaya a la página `M6/6` y configure el número de Canal (Channel) coincidente a su sistema.
  - Presione `SHIFT + REC` para cancelar y regresar al modo predeterminado. El sistema está ahora listo para recibir comandos externos.
- **Envío de Señal (Outgoing MIDI):**
  - El modo Secuenciador de Pasos puede enviar códigos de notas para controlar programas externos u otros instrumentos musicales a través del puerto USB.

## 4.10 Resumen de Teclas de Acceso Rápido

**En Modo Sintetizador Principal y Modo Acorde:**
- Mantenga `CLR + Botón A1` : Ir a la página OSC Frequency
- Mantenga `CLR + Botón A2` : Ir a la página Waveform & Volume
- Mantenga `CLR + Botón B1` : Ir a la página Mod OSC1 & Mod OSC2
- Mantenga `CLR + Botón B2` : Ir a la página Mod OSC3 & Envelope OSC1
- Mantenga `CLR + Botón C1` : Ir a la página Envelope OSC2 & Envelope OSC3
- Mantenga `CLR + Botón C2` : Ir a la página Distortion & Filter

**En Modo Sampler (Abierto usando `SHIFT + CT`):**
- Mantenga `CLR + Botón A1` : Ir a configuración del Sampler Slot 1
- Mantenga `CLR + Botón A2` : Ir a configuración del Sampler Slot 2
- Mantenga `CLR + Botón B1` : Ir a configuración del Sampler Slot 3
- Mantenga `CLR + Botón B2` : Ir a configuración del Sampler Slot 4
- Mantenga `CLR + Botón C1` : Ir a configuración del Sampler Slot 5
- Mantenga `CLR + Botón C2` : Ir a configuración del Sampler Slot 6

## 4.11 Guía de Actualización de Firmware

**Requisitos Previos:**
- Se recomienda usar los navegadores Google Chrome o Microsoft Edge.
- Use exclusivamente cables USB-C preparados para la transmisión de datos (Cables de Datos).
- Si lo conecta al ordenador por primera vez, pudiera ser necesario instalar software para leer el dispositivo (driver `CH9102F / CH34XSER`) con anterioridad.

**Pasos para la Actualización del Software:**
1. Cierre completamente cualquier ventana de plugins (Cura, Serial USB monitors, o programas Arduino IDE) en el ordenador para reducir los problemas de "puerto ocupado".
2. **¡Toque de forma firme y mantenga presionado el botón `B2` en el panel del MON 2!**
3. Mientras su dedo siga pulsando el B2, **presione el interruptor Power (Alimentación) para encender el dispositivo**. La pantalla ha de mantenerse totalmente a oscuras — esto significa que ha entrado correctamente de modo 'Bootloader Flash Mode' a la espera de datos.
4. Visite la página web `https://monkhumcc.github.io/mon2-flash-tool/`
5. Haga clic en la ventana `Connect / Install` (Botón Azul).
6. Espere a que el navegador despliegue una ventana emergente pidiendo el puerto de conexión (Select a Port) - aquí, escoja el puerto *USB-SERIAL*.
7. Apruebe la transmisión de datos. **No desconecte ni jale del cable bajo ninguna circunstancia.** Espere hasta que la carga alcance 100%. El dispositivo se rebotará por sí mismo y estará listo para su uso.

<br><br><br>

---

*(o) MON 2 Soundscape Machine - Engineered in Thailand by Monkhum.cc*
