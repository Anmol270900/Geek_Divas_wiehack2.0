public Camera FirstPersonCamera;
public GameObject CameraTarget;
private Vector3 PrevARPosn;
private bool Track = false;

public void Start() {
  
  PrevARPosn = Vector3.zero;
}

public void Update() {
  UpdateApplicationLifecycle();

 
  Vector3 currentARPosition = Frame.Pose.position;
  if (!Track) {
    Track = true;
    PrevARPosePosition = Frame.Pose.position;
  }
 
  Vector3 deltaPosition = currentARPosition - PrevARPosn;
  PrevARPosn = currARPosn;
  if (CameraTarget != null) {
   
    CameraTarget.transform.Translate(deltaPosition.x, 0.0f, deltaPosition.z);
    
    FirstPersonCamera.GetComponent<ArrowDirection>().targetRot = Frame.Pose.rotation;
  }
}
