Unity Sample Pack Documentation: Music for Motion Film
Overview
Welcome to the Unity Music Sample Pack for Motion Film. This pack contains a curated collection of high-quality music tracks designed to enhance the atmosphere and emotional depth of your cinematic projects. The pack is specifically tailored for use in Unity-based motion films, trailers, cutscenes, or any interactive media project requiring expressive musical scoring.

Whether you're working on action sequences, emotional moments, suspenseful scenes, or ambient environments, this sample pack covers a wide range of styles and moods to complement your visual storytelling.

Features
Format: All tracks are provided in high-quality WAV format (48kHz, 24-bit) for optimal fidelity in professional productions.
Length: Tracks vary in length, with both short and long-form options, allowing flexibility for different scene durations.
Variety of Genres: Includes cinematic orchestral, ambient, electronic, suspense, action, and emotional pieces.
Loopable Tracks: Many tracks are seamlessly loopable for continuous playback in extended scenes.
Layered Sound Design: Some compositions include layered sections, enabling dynamic transitions and adaptability for interactive content.
Royalty-Free License: This music pack is provided under a royalty-free license, allowing unlimited use in commercial and non-commercial projects within Unity without additional fees.
Installation
Importing the Sample Pack
Download the sample pack from the Unity Asset Store or your project repository.
Open your Unity project.
Drag and drop the folder containing the sample pack into your project’s Assets folder.
Once imported, the music tracks will be available under Assets/Music.
Setting Up Music in Unity
Using Music with Audio Source Component
Create an empty GameObject and name it MusicPlayer.
In the Inspector window, click Add Component and choose Audio Source.
Drag and drop your desired music track from the Assets/Music folder into the AudioClip field of the Audio Source component.
Enable Play On Awake if you want the track to start automatically when the scene begins.
Adjust the Volume, Pitch, and Loop settings as needed.
Triggering Music with Scripts
To dynamically trigger music in response to gameplay or events, you can use Unity's scripting API. Here’s a simple script example for changing tracks during runtime:

using UnityEngine;

public class MusicController : MonoBehaviour
{
    public AudioSource audioSource;
    public AudioClip calmMusic;
    public AudioClip actionMusic;

    void Start()
    {
        // Set initial music
        PlayMusic(calmMusic);
    }

    public void PlayMusic(AudioClip clip)
    {
        if (audioSource.isPlaying)
        {
            audioSource.Stop();
        }
        audioSource.clip = clip;
        audioSource.Play();
    }

    // Example of switching to action music
    public void OnActionTriggered()
    {
        PlayMusic(actionMusic);
    }
}

Attach this script to the MusicPlayer GameObject and assign your AudioSource and music tracks via the Inspector.

Layered Music and Dynamic Transitions
For more advanced projects, this sample pack includes layered music tracks. To implement this, you can create separate Audio Source components for each layer (e.g., background ambience, melody, percussion) and adjust their volumes independently for dynamic transitions.

using UnityEngine;

public class LayeredMusicController : MonoBehaviour
{
    public AudioSource backgroundLayer;
    public AudioSource melodyLayer;

    void Start()
    {
        backgroundLayer.Play();
        melodyLayer.Play();
    }

    public void FadeInMelody()
    {
        StartCoroutine(FadeIn(melodyLayer, 1f));
    }

    public void FadeOutMelody()
    {
        StartCoroutine(FadeOut(melodyLayer, 1f));
    }

    private IEnumerator FadeIn(AudioSource audioSource, float duration)
    {
        float startVolume = 0;
        audioSource.volume = startVolume;
        while (audioSource.volume < 1.0f)
        {
            audioSource.volume += Time.deltaTime / duration;
            yield return null;
        }
    }

    private IEnumerator FadeOut(AudioSource audioSource, float duration)
    {
        while (audioSource.volume > 0)
        {
            audioSource.volume -= Time.deltaTime / duration;
            yield return null;
        }
        audioSource.Stop();
    }
}


Directory: C:\Users\selfd\Desktop\New Unity Project\Assets


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
d-----        05/10/2024     13:08                MUSIC FOR MOTION PICTURE - VOL. 1                                    
-a----        05/10/2024     12:17            172 MUSIC FOR MOTION PICTURE - VOL. 1.meta                               


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
d-----        05/10/2024     13:08                Audio                                                                
d-----        05/10/2024     13:11                Demo                                                                 
-a----        05/10/2024     12:16            172 Audio.meta                                                           
-a----        05/10/2024     13:08            172 Demo.meta                                                            


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1\Audio


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
d-----        05/10/2024     12:56                AIFF                                                                 
d-----        05/10/2024     12:56                MP3                                                                  
d-----        05/10/2024     12:57                OGG                                                                  
d-----        05/10/2024     12:57                WAV                                                                  
-a----        05/10/2024     12:34            172 AIFF.meta                                                            
-a----        05/10/2024     12:34            172 MP3.meta                                                             
-a----        05/10/2024     12:34            172 OGG.meta                                                             
-a----        05/10/2024     12:34            172 WAV.meta                                                             


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1\Audio\AIFF


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
-a----        05/10/2024     12:33       44245762 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.aiff                                   
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.aiff.meta                              
-a----        05/10/2024     12:33       84741030 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.aiff                                   
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.aiff.meta                              
-a----        05/10/2024     12:33       70383654 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.aiff                                   
-a----        05/10/2024     12:34            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.aiff.meta                              
-a----        05/10/2024     12:33       22277082 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.aiff                                   
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.aiff.meta                              
-a----        05/10/2024     12:33      124009254 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.aiff                                   
-a----        05/10/2024     12:37            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.aiff.meta                              
-a----        05/10/2024     12:33      205535510 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.aiff                                      
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.aiff.meta                                 
-a----        05/10/2024     12:33       88126142 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.aiff                                      
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.aiff.meta                                 


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1\Audio\MP3


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
-a----        05/10/2024     10:59        4014079 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.mp3                                    
-a----        05/10/2024     12:23            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.mp3.meta                               
-a----        05/10/2024     10:59        7687104 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.mp3                                    
-a----        05/10/2024     12:23            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.mp3.meta                               
-a----        05/10/2024     12:54        4887738 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 3.mp3                                    
-a----        05/10/2024     12:55            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 3.mp3.meta                               
-a----        04/10/2024     17:51        6385161 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.mp3                                    
-a----        05/10/2024     12:23            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.mp3.meta                               
-a----        04/10/2024     17:51        2021667 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.mp3                                    
-a----        05/10/2024     12:23            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.mp3.meta                               
-a----        04/10/2024     17:52       11248952 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.mp3                                    
-a----        05/10/2024     12:23            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.mp3.meta                               
-a----        04/10/2024     11:35       18643904 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.mp3                                       
-a----        05/10/2024     12:22            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.mp3.meta                                  
-a----        04/10/2024     11:33        7994304 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.mp3                                       
-a----        05/10/2024     12:23            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.mp3.meta                                  


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1\Audio\OGG


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
-a----        05/10/2024     12:32        3626089 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.ogg                                    
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.ogg.meta                               
-a----        05/10/2024     12:33        7466946 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.ogg                                    
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.ogg.meta                               
-a----        05/10/2024     12:55        4977289 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 3.ogg                                    
-a----        05/10/2024     12:55            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 3.ogg.meta                               
-a----        05/10/2024     12:33        5577516 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.ogg                                    
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.ogg.meta                               
-a----        05/10/2024     12:33        1762635 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.ogg                                    
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.ogg.meta                               
-a----        05/10/2024     12:33       10036405 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.ogg                                    
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.ogg.meta                               
-a----        05/10/2024     12:33       16848811 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.ogg                                       
-a----        05/10/2024     12:34            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.ogg.meta                                  
-a----        05/10/2024     12:33        7213116 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.ogg                                       
-a----        05/10/2024     12:34            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.ogg.meta                                  


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1\Audio\WAV


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
-a----        05/10/2024     12:32       44245786 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.wav                                    
-a----        05/10/2024     12:35            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 1.wav.meta                               
-a----        05/10/2024     12:32       84741054 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.wav                                    
-a----        05/10/2024     12:37            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 2.wav.meta                               
-a----        05/10/2024     12:52       42840372 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 3.wav                                    
-a----        05/10/2024     12:52            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 3.wav.meta                               
-a----        05/10/2024     12:32       70383678 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.wav                                    
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 4.wav.meta                               
-a----        05/10/2024     12:32       22277106 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.wav                                    
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 5.wav.meta                               
-a----        05/10/2024     12:32      124009278 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.wav                                    
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  STRING QUARTET PIECE NUMBER 6.wav.meta                               
-a----        05/10/2024     12:32      205535534 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.wav                                       
-a----        05/10/2024     12:36            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 1.wav.meta                                  
-a----        05/10/2024     12:32       88126166 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.wav                                       
-a----        05/10/2024     12:34            485 QUANTUM STUDIOS (TIAGO MORAIS MORGADO) - MUSIC FOR MOTION PICTURE -  
                                                  VIOLIN SOLO PIECE NUMBER 2.wav.meta                                  


    Directory: C:\Users\selfd\Desktop\New Unity Project\Assets\MUSIC FOR MOTION PICTURE - VOL. 1\Demo


Mode                 LastWriteTime         Length Name                                                                 
----                 -------------         ------ ----                                                                 
-a----        05/10/2024     13:09          11189 demo - 1.unity                                                       
-a----        05/10/2024     13:09            155 demo - 1.unity.meta                                                  
-a----        05/10/2024     13:10          11184 demo - 2.unity                                                       
-a----        05/10/2024     13:09            155 demo - 2.unity.meta                                                  
-a----        05/10/2024     13:11          11192 demo - 3.unity                                                       
-a----        05/10/2024     13:09            155 demo - 3.unity.meta                                                  
-a----        05/10/2024     13:11          11184 demo - 4.unity                                                       
-a----        05/10/2024     13:09            155 demo - 4.unity.meta                                                  

You are free to use the tracks in your Unity projects, both commercial and non-commercial.
Attribution is not required, but appreciated where possible.
Support
For any questions, troubleshooting, or additional requests regarding this sample pack, please contact our support team at [selfdeterminedhermit@gmail.com].

Thank you for using the Unity Music Sample Pack for Motion Film. We hope these tracks help elevate your project’s cinematic experience!