using System.Collections;
using System.Collections.Generic;
using Mirror;
using UnityEngine;

public class MardNetworkPlayer : NetworkBehaviour
{
    [SyncVar]
    [SerializeField]
    private string displayName = "Natthaphon Chawnamon";

    [SyncVar]
    [SerializeField]
    private Color displayColour = Color.black;

    [Server]
    public void SetDisplayName(string newDisplayName)
    {
        displayName = newDisplayName;
    }

    [Server]
    public void SetDisplayColour(Color newDisplayColour)
    {
        displayColour = newDisplayColour;
    }
}
